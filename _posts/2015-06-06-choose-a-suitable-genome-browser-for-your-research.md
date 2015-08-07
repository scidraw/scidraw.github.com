---
layout: post
title: "Choose a suitable genome browser for your research"
description: "genome browser will benefit your studies so much"
tagline: by Luye & zhoujj
category: Draw
tags: [genomebrowser]
---
{% include JB/setup %}

To show your result, you need snapshot of genome in details apart from chart and statistics plot. Because everybody want to see the details of the genome. The global view of genome can only draw a global conclusion.

为了展示项目结果，科研工作者除了要用一些图表来展示结果外，经常要画一些展示细节的图表。因为展示整体结果还是不够的，很多人会想看到具体细节的图表。也就是说你要展示一些实例。

<!--more-->

## UCSC genome browser

This is the best genome browser in the world. You can visit [UCSC](https://genome.ucsc.edu).

You can also set up a standalone version, but the steps are a little complicated.

[Standalone UCSC browser configuration]()


## Jbrowse

[Jbrowse](http://jbrowse.org) is a fast, embeddable genome browser built completely with JavaScript and HTML5, with optional run-once data formatting tools written in Perl. 

I have write a [post](http://scidraw.github.io/bioinformatics/2014/07/13/jbrowser-installation/) about standalone version configuration.

[Jbrowse source code](http://jbrowse.org/jbrowse-1-11-6/)

## Dalliance: a genome browser build by node.js

It easy to upload track to genome browser and get publication level image, but it only support a few data format. Another feature is that it didn't need server configuration. JS only require client web browser support.

Currently-supported formats are:

+ bigBed (make from a BED file using bedToBigBed)

+ bigWig (make from a WIG fiel using wigToBigWig)

+ BAM (can be produced from most sequence alignment formats using, e.g., samtools

+ .2bit (only for reference genomes)


[local install]()

[More details about biodalliance](http://www.biodalliance.org)

[Source code](https://github.com/dasmoth/dalliance)

## IGV

IGV is good software for desktop user.

Download: [http://www.broadinstitute.org/software/igv/home](http://www.broadinstitute.org/software/igv/home)


