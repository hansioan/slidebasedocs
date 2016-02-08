---
title: Search for promoters by location
taxonomy:
    category: docs
---

In addition to promoter expression, we can also set location constraints based on the genomic location of promoters to further refine our search. 

The location search offers the option to search for promoters at specific genomic locations or at locations given by known genes.

There are two ways to set the location search information:

##### Basic
**Directly setting the specific sites (Basic):** You can choose all or a specific chromosome from the **Chromosome** dropdown menu and input a **Start Site**, an **End Site** and a **Strand** in the corresponding text boxes. This will be the searching range. When choosing a chromosome, the starting site will contain the value 1, the ending site will contain the size of the chromosome on both strands.
![](/images/promoters/location-ex0.png)

##### Gene Based

**Searching around interested genes:** There are two types of gene-based search: **Gene** and **Gene + Transcript:**

+ **Gene:** You can type a gene name (RefSeq gene ID) in the **Genes** box, and select the desired gene based on its name. Gene name suggestions will be given based on your input. When a gene name is selected, SlideBase will look for promoters around the location of that gene. More exactly SlideBase will look for promoters within the boundaries (from transcription start site to transcription end site) of that gene. Since a gene may have multiple transcripts, which may differ in locations, and because in some cases a gene name can have locations on different chromosomes, SlideBase will search at the union of all the locations of genes with the same given name. 

    Additionally gene locations can be padded upstream and downstream to expand the search from gene boundaries to also include locations near the genes. By default the gene coordinates are expanded upstream and downstream by 100 kilobases as show in the **Upstream** and **Downstream** text boxes.

    ![](/images/promoters/location-ex3-1.png)

+ **Gene + Transcript:** You can type a gene name (RefSeq gene ID) in the **Genes** box, and select the desired gene based on its name. Gene name suggestions along with its transcript IDs and exact genomic locations will be given based on your input. When a gene name is selected, SlideBase will look for promoters around the location given by the gene name - transcript pair. In this case the gene name - transcript pair will uniquely identify a genomic location. After choosing a gene from the suggestions list, the details about gene transcript and location (chromosome, start site, end site and strand) will be displayed in the bottom area of the location panel. 
    
    ![](/images/promoters/location-ex5.png)
    
    Additionally gene locations can be padded upstream and downstream to expand the search from gene boundaries to also include locations near the genes. By default the gene coordinates are expanded upstream and downstream by 100 kilobases as show in the **Upstream** and **Downstream** text boxes.

    ![](/images/promoters/location-ex6.png)

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! Each location search option is displayed in its own tab. The location parameters used in the search will correspond to those present in the current selected location tab (selected tab denotes the search, other tabs are ignored).  

The location search can be disabled by clicking the **Disable** button on the top-right corner. Disabling the location search implies that the search will be conducted among all the chromosomes with no restriction on the start or end site, nor on any gene related locations.

#### Examples
The examples below showcase the promoter location selector. The number of promoters resulting only depends on their location and not on any expression constraints, although these can be combined.

##### Example 1:
**Promoters located on chromosome 5**

![](/images/promoters/location-ex1-1.png)

To select promoters located on chromosome 5 click on the **Chromosome** dropdown menu from the basic location panel and select "chr5". The **Start Site** will contain the value 1 and the **End Site** will contain the value of the size of chromosome 5. This results in 9171 promoters.

If we only take into account the promoters on the plus strand we obtain 4793 promoters.

![](/images/promoters/location-ex1-2.png)

##### Example 2:
**Custom start and end sites on chromsome 1**
![](/images/promoters/location-ex2.png)

After selecting promoters located on chromosome 1 (both strands), we can use custom **Start Site** and **End Site**. In this example we have chosen the start site to be 1,000,000 and the end site to be 2,000,000. This results in 2348 promoters.

##### Example 3:
** Promoters located near the "RUNX1" gene**

In the "Gene" panel, type in RUNX1 in the **Genes** textbox. Choose "RUNX1" from the suggestions menu.
![](/images/promoters/location-ex3-2.png)

The default **Upstream** and **Downstream** pad values are set to 100,000.

![](/images/promoters/location-ex3-3.png)

The number of promoters within 100,000 bases around all RUNX1 gene locations is 51.

##### Example 4:
** Promoters located within the boundaries of all RUNX1 gene locations**

![](/images/promoters/location-ex4.png)

This is achieved by setting the **Upstream** and **Downstream** pad values to 0. The resulting number of promoters is 47.

##### Example 5

** Promoters located near the "RUNX1" gene for a specific transcript**
In the "Gene + Transcript" panel, type in RUNX1 in the **Genes** textbox. Choose the first occurence of "RUNX1"  from the suggestions menu with the trascript id of "uc002yuh.3"

![](/images/promoters/location-ex5.png)

After selecting the gene-transcript pair, the exact location and transcript id will be displayed in the bottom of the "Gene + Transcript" panel. Similar to the regular gene selection, we have the option of padding the gene boundaries. By default, the **Upstream** and **Downstream** pad values are set to 100,000. The resulting number of promoters within 100,000 bases of the RUNX1 gene with the "uc002yuh.3" transcript is 28.



