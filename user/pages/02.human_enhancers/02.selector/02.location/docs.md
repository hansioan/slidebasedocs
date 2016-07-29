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
![](/images/enhancers/location-ex0.png)

##### Gene Based

**Searching around interested genes:** There are two types of gene-based search: **Gene** and **Gene + Transcript:**

+ **Gene:** You can type a gene symbol in the **Genes** box, and select the desired gene based on its name. Gene name suggestions will be given based on your input. When a gene name is selected, SlideBase will look for promoters around the TSS location of that gene. By default, the area around the gene TSS is 100 kilobases upstream and 100 kilobases downstream. This area around the TSS can be changed by modifying the values in the **Upstream** and **Downstream** text boxes. The upstream and downstream padding values are adjusted according to the gene strand. 

	!!! <i class="fa fa-exclamation-circle"></i> **Note:**
	!!!
	!!! Since a gene may have multiple transcripts, which may differ in locations, and because in some cases a gene name can have locations on different chromosomes, SlideBase will search at the union of all the TSS locations of genes with the same given name.  Similar to above, the area around the gene transcripts will be given by the upstream and downstream values. 


	![](/images/promoters/location-ex3-1.png)

+ **Gene + Transcript:** You can type a gene symbol in the **Genes** box, and select the desired gene based on its name. Gene name suggestions along with its transcript IDs and exact genomic locations will be given based on your input. When a gene name is selected, SlideBase will look for promoters around the  TSS location given by the gene name - transcript pair and the values in the **Upstream** and **Downstream** text boxes. In this case the gene name - transcript pair will uniquely identify a genomic location. After choosing a gene from the suggestions list, the details about gene transcript and location (chromosome, start site, end site and strand) will be displayed in the bottom area of the location panel. The upstream and downstream padding values are adjusted according to the gene strand. 
    
    ![](/images/promoters/location-ex5.png)
    
    The **Gene + Transcript** search option is mainly used to search around a precise location given by a specific gene-transcript pair.
    ![](/images/enhancers/location-ex6.png)

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! Each location search option is displayed in its own tab. The location parameters used in the search will correspond to those present in the current selected location tab (selected tab denotes the search, other tabs are ignored).  

The location search can be disabled by clicking the **Disable** button on the top-right corner. Disabling the location search implies that the search will be conducted among all the chromosomes with no restriction on the start or end site, nor on any gene related locations.

#### Examples
The examples below showcase the enhancer location selector. The number of enhancers resulting only depends on their location and not on any expression constraints, although these can be combined.

##### Example 1:
**Enhancers located on chromosome 5**

![](/images/enhancers/location-ex1.png)

To select enhancers located on chromosome 5 click on the **Chromosome** dropdown menu from the basic location panel and select "chr5". The **Start Site** will contain the value 1 and the **End Site** will contain the value of the size of chromosome 5. This results in 1775 enhancers.


##### Example 2:
**Custom start and end sites on chromsome 1**
![](/images/enhancers/location-ex2.png)

After selecting enhancers located on chromosome 1, we can use custom **Start Site** and **End Site**. In this example we have chosen the start site to be 1,000,000 and the end site to be 2,000,000. This results in 18 enhancers.

##### Example 3:
** Enhancers located near the "RUNX1" gene TSS**

In the "Gene" panel, type in RUNX1 in the **Genes** textbox. Choose "RUNX1" from the suggestions menu.
![](/images/enhancers/location-ex3-2.png)

The default **Upstream** and **Downstream** pad values are set to 100,000.

![](/images/enhancers/location-ex3-3.png)

The number of enhancers within 100,000 bases around all RUNX1 gene TSS locations is 24.


##### Example 4

** Enhancers located near the "RUNX1" gene TSS for a specific transcript**
In the "Gene + Transcript" panel, type in RUNX1 in the **Genes** textbox. Choose the first occurence of "RUNX1"  from the suggestions menu with the trascript id of "uc002yuh.3"

![](/images/enhancers/location-ex5.png)

After selecting the gene-transcript pair, the exact location and transcript id will be displayed in the bottom of the "Gene + Transcript" panel. By default, the **Upstream** and **Downstream** pad values are set to 100,000. The resulting number of enhancers within 100,000 bases of the RUNX1 gene TSS with the "uc002yuh.3" transcript is 17.



