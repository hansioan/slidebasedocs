---
title: miRNA Results
taxonomy:
    category: docs
---

### This section describes the [viewer page](http://slidebase.binf.ku.dk/human_mirna/results) for miRNA. 


Based on the expression and/or genomic location constraints, the number of resulting miRNA will differ. After selecting your search options from the [search page](http://slidebase.binf.ku.dk/docs/human_mirna/selector) and clicking the **See Detailed Results >>** (or the smaller **"view"** popup link) link, the user will be directed to the viewer page.

The viewer page displays detailed information about the resulting miRNAs and allows the user to perform actions on the resulting set such as downloading and viewing in genome browsers. The complete set of miRNA information and actions are displayed below.

Your selected miRNA are shown on the list to the left. A maximum number of 50 miRNA are displayed on each page. You can use the **First**, **Prev**, **Next** and **Last** buttons located under the miRNA list and at the bottom of the page to view a different subset. Clicking on an miRNA shows information about that individual miRNA as three different sheets (tabs): **Expression Details** for expression, **Browse** for genome browser views and **View Overlaps** for basal overlaps with SNPs. It is also possible to analyze all selected miRNAs (see below).

### Single miRNA information

This section describes the vizualization / analyses / overlaps for a single miRNA. Each option presented below corresponds to one of the sheets (tabs) available on the viewer page.

##### Expression Details

This view shows the miRNA expression. Specifically, percentage and expression tables for primary cells and libraries (actual sample level expression for all the samples that make up each facet) are available.

The sample wise expression table contains links to [SSTAR](http://fantom.gsc.riken.jp/5/sstar/) which holds detailed information about each sample. Most table columns can be sorted by clicking on the table column header.

##### Browse

This enables the creation of a custom track of your selected miRNA in the [UCSC Genome Browser](http://genome.ucsc.edu/). The UCSC browser has the option of coloring tracks, and houses a larger amount of different data types.

##### View Overlaps

A miRNA-SNP overlap occurs when the SNP location is within the miRNA genomic location boundaries. If a miRNA-SNP overlap exists the SNP can be further inspected by clicking on the SNP id.

### Multiple miRNA information

**Visualization/analyses of multiple selected miRNAs**

Instead of selecting a single miRNAs, a number of analyses options are available for the whole set of resulting miRNAs, shown above the miRNAs list:

+ **Download all** found miRNAs as BED files.

+ **View all** found miRNAs in the UCSC Genome Browser: Input UCSC track information such as name, description and color and view the miRNAs as a custom track in the [UCSC Genome Browser](http://genome.ucsc.edu/).

+ **Get DNA Sequences** for all found miRNAs. In addition to the miRNAs sequences given by their genomic coordinates, a maximum of 100 extra nucleotides can be added to each the 5' and 100 nucleotides to the 3' end of each individual miRNA sequence.

+ **Motif Discovery**: Perform basic motif discovery on the resulting miRNA sequences using the [MEME motif discovery tool](http://meme-suite.org/). The miRNA sequences can be padded with a maximum of 100 extra nucleotides on the 5' and 100 on the 3' ends. The MEME job will be sent via email if the user inputs a valid email address.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**  
!!!
!!! The online version of MEME only accepts a maximum of 1,000 sequences which in total must not exceed 60,000 nucleotides.  All sequences must be longer than 8 nucleotides.