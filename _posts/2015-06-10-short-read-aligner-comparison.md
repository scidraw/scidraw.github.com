---
layout: post
title: "Short reads (Next generation sequencing reads) aligner comparison"
description: "How to choose the best aligner for your research"
tagline: by Luye & zhoujj
category: bioinformatics
tags: [alignment]
---
{% include JB/setup %}

Different studies require different alignment tools. Which alignment tool is better, depends on what you want to analysis. There many alignment tools, BWA, Soapaligner, Bowtie2 ranked at the top.

<!--more-->

### HengLi stat that BWA is better to find the uniqe mapped position compare to bowtie2

[http://seqanswers.com/forums/showthread.php?t=15200](http://seqanswers.com/forums/showthread.php?t=15200)

[http://lh3lh3.users.sourceforge.net/alnROC.shtml](http://lh3lh3.users.sourceforge.net/alnROC.shtml)

Maq is the first software for short reads alignment, then BWA replace maq to be the most widely used software in the world. BWA allow mismatch and 0-9 small indel in alignment. 

In most of the studies, they only want to detect the SNVs and small indels, so a lot of people tend to use BWA as aligner.

Additionaly, BWA is a mature software, people are tend to believe BWA result.


### Bowtie2 is also a good choice

[http://www.genomebiology.com/2009/10/3/R25](http://www.genomebiology.com/2009/10/3/R25)

[http://www.nature.com/nmeth/journal/v9/n4/full/nmeth.1923.html](http://www.nature.com/nmeth/journal/v9/n4/full/nmeth.1923.html)

Bowtie2 permited longer indels in alignment and SNVs result is similar to BWA and other aligner.


### TOPHAT for RNA-seq short reads alignment

[https://ccb.jhu.edu/software/tophat/index.shtml](https://ccb.jhu.edu/software/tophat/index.shtml)

There is no doubt that TOPHAT is the best aligner for RNA-seq data or RNA sequencing reads.

rsem, htseq used other method for alignment.

### Which strategy do I prefer?

For DNA short reads alignment, I prefer bowtie2; (although someone stat that BWA is more accracy that bowtie2)

For RNA short reads alignment, I prefer Tophat;


