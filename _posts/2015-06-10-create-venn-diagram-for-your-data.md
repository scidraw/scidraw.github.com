---
layout: post
title: "Create venn diagram for your data analysis"
description: "How to create venn diagram for your reserach"
tagline: by Luye & zhoujj
category: draw
tags: [venn]
---
{% include JB/setup %}

Biology is a complexity field. We have many element inside a cell, tissue and organ. For classification, we seperate the genome into many parts, then for exploring. For two Chip-seq data analysis, we want to compare the difference/overlap of these tow independent experiments. So we need venn diagram.

<!--more-->

## Some software for venn diagram 

### R package

https://r-forge.r-project.org/scm/viewvc.php/*checkout*/pkg/Vennerable/inst/doc/Venn.pdf?revision=58&root=vennerable

### An online venn diagram program

http://bioinformatics.psb.ugent.be/webtools/Venn/


## Calculate value for 3 set Venn diagram

Suppose we three set of gene, each list contain uniq gene id with the list. We treat these three set as a, b and c, respectively. Then we want to calculate: a, b, c, a+b+c, a+b-c, a+c-b, b+c-a, a-b-c, b-a-c, c-a-b. These calculations match different areas of venn diagram like this:

![venn diagram example]()

### for gene list

A perl script can do this:

{% highlight perl %}
my ($a, $b, $c, $col) = @ARGV;

pop(@ARGV);

print "a: $a\n";
print "b: $b\n";
print "c: $c\n";

my %all;
my %sep;

my %index = (
	"0"=>"a",
	"1"=>"b",
	"2"=>"c",
);

my $i = 0;
foreach my $f (@ARGV){
	open IN,"$f" || die $!;
	while(<IN>){
		chomp;
		my @t = split /\t/;
		$all{$t[0]} = 1;
		$sep{$index{$i}}{$t[0]} = 1;
	}
	close IN;
	$i++;
}

### a & b & c
my @abc;
my @ab;
my @ac;
my @bc;

my @a_b_c;
my @b_a_c;
my @c_a_b;

foreach my $id (keys %all){
	if(exists $sep{'a'}{$id} && exists $sep{'b'}{$id} && exists $sep{'c'}{$id}){
		push @abc,$id;
	}
	if(exists $sep{'a'}{$id} && exists $sep{'b'}{$id} && !(exists $sep{'c'}{$id})){
		push @ab,$id;
	}
	if(exists $sep{'a'}{$id} && !(exists $sep{'b'}{$id}) && exists $sep{'c'}{$id}){
		push @ac,$id;
	}
	if(!(exists $sep{'a'}{$id}) && exists $sep{'b'}{$id} && exists $sep{'c'}{$id}){
		push @bc,$id;
	}
	if(exists $sep{'a'}{$id} && !(exists $sep{'b'}{$id}) && !(exists $sep{'c'}{$id})){
		push @a_b_c,$id;
	}
	if(!(exists $sep{'a'}{$id}) && exists $sep{'b'}{$id} && !(exists $sep{'c'}{$id})){
		push @b_a_c,$id;
	}
	if(!(exists $sep{'a'}{$id}) && !(exists $sep{'b'}{$id}) && exists $sep{'c'}{$id}){
		push @c_a_b,$id;
	}
}
print "\n";
print "a: ".scalar(keys %{$sep{'a'}})."\n";
print "b: ".scalar(keys %{$sep{'b'}})."\n";
print "c: ".scalar(keys %{$sep{'c'}})."\n";
print "\n";
print "a+b+c: ".scalar(@abc)."\n";
print "\n";
print "a+b-c: ".scalar(@ab)."\n";
print "a+c-b: ".scalar(@ac)."\n";
print "b+c-a: ".scalar(@bc)."\n";
print "\n";
print "a-b-c: ".scalar(keys @a_b_c)."\n";
print "b-a-c: ".scalar(keys @b_a_c)."\n";
print "c-a-b: ".scalar(keys @c_a_b)."\n";
open OUT,">","a+b+c.lst" || die $!;
foreach my $id (@abc){
	print OUT "$id\n";
}
close OUT;

open OUT,">","a+b-c.lst" || die $!;
foreach my $id (@ab){
	print OUT "$id\n";
}
close OUT;

open OUT,">","a+c-b.lst" || die $!;
foreach my $id (@ac){
	print OUT "$id\n";
}
close OUT;

open OUT,">","b+c-a.lst" || die $!;
foreach my $id (@bc){
	print OUT "$id\n";
}
close OUT;

open OUT,">","a-b-c.lst" || die $!;
foreach my $id (@a_b_c){
    print OUT "$id\n";
}
close OUT;

open OUT,">","b-a-c.lst" || die $!;
foreach my $id (@b_a_c){
    print OUT "$id\n";
}
close OUT;

open OUT,">","c-a-b.lst" || die $!;
foreach my $id (@c_a_b){
    print OUT "$id\n";
}
close OUT;

my $a_base = basename($a,".lst");
my $b_base = basename($b,".lst");
my $c_base = basename($c,".lst");
{% endhighlight %}

### for region list

To create a venn diagram from region list is a little arbitrary. Because a region in A many include several regions in B, it will contain 2 different values to represent the overlap part.

We utilied bedtools and pybedtools to implement the calculation of 3 set region venn diagram.

{% highlight perl %}

{% endhighlight %}


Why I don't use the package from R or online website, because I want clearly know what analysis I am doing.


