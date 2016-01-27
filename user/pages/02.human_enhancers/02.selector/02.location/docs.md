---
title: Search for enhancers by location
taxonomy:
    category: docs
---

In addition to enhancer expression, we can also set location constraints based on the genomic location of enhancers to further refine our search. 

The location search offers the option to search for enhancers at specific genomic locations or at locations given by known genes.  Since enhancers are bidirectionally transcribed they have no associated strand (** + ** or ** - **).

There are two ways to set the location search information:

##### Basic
**Directly setting the specific sites (Basic):** You can choose all or a specific chromosome from the **Chromosome** dropdown menu and input a **Start Site** and an **End Site** in the corresponding text boxes. This will be the searching range. When choosing a chromosome, the starting site will contain the value 1 and the ending site will contain the size of the chromosome.

##### Gene Based

**Searching around interested genes:** There are two types of gene-based search: **Gene** and **Gene + Transcript:**

+ **Gene:** You can type a gene name (refseq gene ID) in the **Genes** box, and select the desired gene based on its name. Gene name suggestions will be given based on your input. When a gene name is selected, SlideBase will look for enhancers around the location of that gene. More exactly SlideBase will look for enhancers within the boundaries (from transcription start site to transcription end site) of that gene. Since a gene may have multiple transcripts, which may differ in locations, and because in some cases a gene name can have locations on different chromosomes, SlideBase will search at the union of all the locations of genes with the same given name. 

    Additionally gene locations can be padded upstream and downstream to expand the search from gene boundaries to also include locations near the genes. By default the gene coordinates are expanded upstream and downstream by 100 kilobases as show in the **Upstream** and **Downstream** text boxes.

+ **Gene + Transcript:** You can type a gene name (refseq gene ID) in the **Genes** box, and select the desired gene based on its name. Gene name suggestions along with its transcript IDs and exact genomic locations will be given based on your input. When a gene name is selected, SlideBase will look for enhancers around the location given by the gene name - transcript pair. In this case the gene name - transcript pair will uniquely identify a genomic location. After choosing a gene from the suggestions list, the details about gene transcript and location (chromosome, start site, end site and strand) will be displayed in the bottom area of the location panel. 

    Additionally gene locations can be padded upstream and downstream to expand the search from gene boundaries to also include locations near the genes. By default the gene coordinates are expanded upstream and downstream by 100 kilobases as show in the **Upstream** and **Downstream** text boxes.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! Each location search option is displayed in its own tab. The location parameters used in the search will correspond to those present in the current selected location tab (selected tab denotes the search, other tabs are ignored).  

The location search can be disabled by clicking the **Disable** button on the top-right corner. Disabling the location search implies that the search will be conducted among all the chromosomes with no restriction on the start or end site, nor on any gene related locations.

