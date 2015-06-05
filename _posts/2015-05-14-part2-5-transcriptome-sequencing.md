---
layout: post
title: "[Part2-4] Transcriptome sequencing"
description: ""
tagline: by Luye & zhoujj
category: bioinformatics
tags: [RNA-seq, tutorial]
---
{% include JB/setup %}

The post will highlight some tips for transcriptome sequencing project. Every people have a different genome, Every tissue/cell in human body have dramatic pattern in different time. So it is difficut to draw the map/behavior of all gene element in our genome. To get a high quality profile RNA is the beginning to explor the biological world.

<!--more-->

### Which kind of RNA-seq in suitable for your project?

For all trasncript studies, total RNA(rRNA depletion) sequencing is suitable.

For protein coding gene studies, polyA RNA sequencing is suitable.

For transcriptome require strand information, strand-specific RNAseq in suitable.

### How much data do we need?

For protein coding message RNA quantification studies(gene level quantification), 10M~20M fragments per sample is sufficient for most gene-based comparisons.

For lncRNA and protein coding message RNA quantification studies(isoform level), 50M~100M fragments per sample is sufficient for mutiple sample comparisons.

For lncRNA and protein coding message RNA assembly/Alternative splicing/Allele Specific Expression analysis, 100M+ fragments is needed for analysis.

For lncRNA and protein coding message RNA denovo assembly and quantification, 100M+ fragments is needed to reconstruct the structure of expressed transcripts.

A powerful tool for RNA-seq experiment design:

[scotty](http://bioinformatics.bc.edu/marthlab/scotty/scotty.php)

[How deep is deep enough for RNA-Seq profiling of bacterial transcriptomes?](http://www.biomedcentral.com/1471-2164/13/734)

### Some QC tools

http://code.google.com/p/rseqc/



### Before transcript quantification, exists a ref genome/transcript or de novo assembly?



### RNA-seq data analysis protocols(quantification)

[RPM/RPKM](http://bioviz.org/pollen/A_thaliana_Jun_2009/SupplementalDataFiles/SupplementalDataFiles1to3.html)

[gffread](http://cole-trapnell-lab.github.io/cufflinks/file_formats/)


### Differential expression gene detection (SNPs/Alterative Splicing/long noncoding RNA)



### Function analysis for the differential expression genes




### Related papers

1. [Mapping and quantifying mammalian transcriptomes by RNA-Seq](http://www.nature.com/nmeth/journal/v5/n7/pdf/nmeth.1226.pdf)

2. [Full-length transcriptome assembly from RNA-Seq data without a reference genome](http://www.nature.com/nbt/journal/v29/n7/full/nbt.1883.html)

3. [http://www.nature.com/nprot/journal/v7/n3/full/nprot.2012.016.html](http://www.nature.com/nprot/journal/v7/n3/full/nprot.2012.016.html)

4. [Ab initio reconstruction of cell type-specific transcriptomes in mouse reveals the conserved multi-exonic structure of lincRNAs](http://www.nature.com/nbt/journal/v28/n5/full/nbt.1633.html)

5. [Integrated genomic characterization of endometrial carcinoma](http://www.nature.com/nature/journal/v497/n7447/full/nature12113.html)

6. [Sailfish enables alignment-free isoform quantification from RNA-seq reads using lightweight algorithms](http://www.nature.com/nbt/journal/v32/n5/full/nbt.2862.html)



### Some material for RNA sequencing

[RNA-seqlopedia](http://rnaseq.uoregon.edu/)

[Standards, Guidelines and Best Practices for RNA-Seq](http://genome.ucsc.edu/ENCODE/protocols/dataStandards/ENCODE_RNAseq_Standards_V1.0.pdf)

[RNA_Seq_FAQ.aspx](http://www.genewiz.com/public/RNA_Seq_FAQ.aspx)

[What is RNA-Seq?](http://www.agrf.org.au/resources/next-gen-resources/ngs-faqs#What is RNA-Seq?)

[RNA-Seq SeqAnswers](http://seqanswers.com/forums/showthread.php?t=15440)
