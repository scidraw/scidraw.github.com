---
layout: post
title: "Setting up a private CPAN library"
description: "Setting up a private CPAN library"
tagline: by Luye & zhoujj
category: bioinformatics
tags: [perl, cpan]
---
{% include JB/setup %}

Setting up a private CPAN library - without admin privileges

<!--more-->

### run CPAN

perl -MCPAN -e shell


### configuration

$ cd ~
$ perl -MCPAN -e shell

Input the follow content:

{% highlight bash %}
o conf make_arg -I/home/zhoujj/lib/CPAN
o conf make_install_arg -I/home/zhoujj/lib/CPAN
o conf makepl_arg "install_base=/home/zhoujj/lib/CPAN LIB=/home/zhoujj/lib/CPAN/lib INSTALLPRIVLIB=/home/zhoujj/lib/CPAN/lib INSTALLARCHLIB=/home/zhoujj/lib/CPAN/lib/arch INSTALLSITEARCH=/home/zhoujj/lib/CPAN/lib/arch INSTALLSITELIB=/home/zhoujj/lib/CPAN/lib INSTALLSCRIPT=/home/zhoujj/lib/CPAN/bin INSTALLBIN=/home/zhoujj/lib/CPAN/bin INSTALLSITEBIN=/home/zhoujj/lib/CPAN/bin INSTALLMAN1DIR=/home/zhoujj/lib/CPAN/man/man1 INSTALLSITEMAN1DIR=/home/zhoujj/lib/CPAN/man/man1 INSTALLMAN3DIR=/home/zhoujj/lib/CPAN/man/man3 INSTALLSITEMAN3DIR=/home/zhoujj/lib/CPAN/man/man3"
o conf commit
{% endhighlight %}

### setting up perl lib path

Add this content to ~/.bashrc or ~/.bash_profile

{% highlight bash %}
export PERL5LIB=/home/zhoujj/lib/CPAN/lib 
{% endhighlight %}

