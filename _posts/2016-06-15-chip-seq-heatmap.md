---
layout: post
title: "chip seq heatmap"
description: ""
tagline: by Luye & zhoujj
category: draw 
tags: [bioinformatics draw]
---
{% include JB/setup %}

I am rather new to the bioinformatics field, and much of my current work has been on the analysis and visualization of individual ChIP-Seq data or in combination with other sequencing data. A large part of this is the generation of heatmaps that accurately represent our the data in defined regions, yet are attractive and require little to no altering for publishing purposes.

<!--more-->

Introduction
I am rather new to the bioinformatics field, and much of my current work has been on the analysis and visualization of individual ChIP-Seq data or in combination with other sequencing data. A large part of this is the generation of heatmaps that accurately represent our the data in defined regions, yet are attractive and require little to no altering for publishing purposes.

Problem
The visualization of data is important. Various different tools have been created to allow the visualization of said data. But no two tools are the same regardless of the same input data / format. Why is this?

What other tools are you aware of for producing heatmaps?

Tools
Deeptools: https://github.com/fidelram/deepTools
Ngsplot: https://github.com/shenlab-sinai/ngsplot
ChAsE: http://chase.cs.univie.ac.at/overview
HOMER: http://homer.salk.edu/homer/
genomation: https://bioconductor.org/packages/devel/bioc/html/genomation.html
SeqPlots: https://github.com/Przemol/seqplots
EaSeq: http://easeq.net/
Results
The following section will consist of the heatmaps produced by each program to identify aesthetic differences.

The heatmaps will consist of Pol II N20 ChIP-Seq data overlapped to a dataset of 20,345 Gencode protein_coding genes looking specifically the TSS and a -2000/+2000 region surrounding the TSS. A binsize of 25 will be used for all of the tools (when applicable) unless otherwise stated to keep test times to a minimum. I will attempt to keep the images as close together in size as possible (I do not know if this bares any significance in the outlook of a heatmap). For sorting I will be using mean signal intensity, for those tools that do not have a method for computing the mean for each row in a matrix, I will be using the max method. I will attempt to use bigWig files whenever possible to keep results due to error in file type processing to a minimum, but this is completely out of my control.

It is important to note some of the tools appear to require pre-processing of the dataset, while others accept bedfiles easily and give the option of choosing a region to plot.


