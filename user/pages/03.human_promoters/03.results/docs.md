---
title: Promoter Results
taxonomy:
    category: docs
---

### This section describes the [viewer page](http://slidebase.binf.ku.dk/human_promoters/results) for promoters. 

Based on the expression and/or genomic location constraints, the number of resulting promoters will differ. After selecting your search options from the [search page](http://slidebase.binf.ku.dk/docs/human_promoters/selector) and clicking the **See Detailed Results >>**  (or the smaller **"view"** popup link) link, the user will be directed to the viewer page. 

The viewer page displays detailed information about the resulting promoters and allows the user to perform actions on the resulting set such as downloading and viewing in genome browsers.  The complete set of promoter information and actions are displayed below.

Your selected promoters are shown on the list to the left. A maximum number of 50 promoters are displayed on each page. You can use the **First**, **Prev**, **Next** and **Last** buttons located under the promoter list and at the bottom of the page to view a different subset. Clicking on an promoter shows information about that individual promoter as three different sheets (tabs): **CAGE Details** for expression, **Browse** for genome browser views and **View Overlaps** for basal overlaps and correlations with proximal genomic entities. It is also possible to analyze all selected promoters (see below). 


### Single promoter information

This section describes the vizualization / analyses / overlaps for a single promoter. Each option presented below corresponds to one of the sheets (tabs) available on the viewer page. 

##### CAGE Details
This view shows the promoter expression along with annotation information. Specifically, percentage and expression tables for primary cells (facets), organs (facets) and libraries (actual sample level expression for all the samples that make up each facet) are available. 

The annotation section (section 1) describes basic FANTOM5 promoter information. These inform if the promoter is associated with known genes or is a novel promoter. If the promoter is associated with a known gene, in most cases there will be external links to resources which describe information about that specific gene. The resources are: 
    - [NCBI Entrez Genes](http://www.ncbi.nlm.nih.gov/gene) 
    - [HUGO Gene Nomenclature Comittee (HGNC)](http://www.genenames.org/)
    - [Universal Protein Resource (UniProt)](http://www.uniprot.org/uniprot/)
    - [SSTARR](http://fantom.gsc.riken.jp/5/sstar/)


The sample wise expression table contains links to [SSTAR](http://fantom.gsc.riken.jp/5/sstar/) which holds detailed information about each sample. Most table columns can be sorted by clicking on the table column header.

##### Browse
This enables the creation of a custom track of your selected promoters in either the [UCSC Genome Browser](http://genome.ucsc.edu/) or the [ZENBU Genome Browser](http://fantom.gsc.riken.jp/zenbu/).  The UCSC browser has the option of coloring tracks, and houses a larger amount of different data types. ZENBU, on the other hand, has the advantage of showing actual expression levels of CAGE data with advanced mouse-over functions. 


##### View Overlaps
This shows predicted enhancer(s) targeted by the promoter, and SNP overlaps.  Enhancer-promoter pairs are predicted based on genomic distance and CAGE co-expression, expressed as Pearson’s correlation tests. An enhancer-promoter prediction is shown when the distance from an enhancer center to a TSS summit is within 500 kbp and the Pearson correlation adjusted P-value (FDR) is < 10 <sup>-5</sup> (as in [Andersson et al.](http://dx.doi.org/doi:10.1038/nature12787) ). If an enhancer-promoter overlap exists, the enhancer can be further inspected by clicking on the enhancer annotation and going to SlideBase [enhancer results page](http://slidebase.binf.ku.dk/docs/human_enhancers/results) for that enhancer. 

A promoter-SNP overlap occurs when the distance from a promoter summit and a SNP location is within 300 bp upstream and 100 bp downstream the promoter summit.  If a promoter-SNP overlap exists the SNP can be further inspected by clicking on the SNP id.


### Multiple promoter information

**Visualization/analyses of multiple selected promoters**

Instead of selecting a single promoter, a number of analyses options are available for the whole set of resulting promoters, shown above the promoter list:



+ **Download all** found promoters as BED files.

+ **View all** found promoters in the UCSC Genome Browser: Input UCSC track information such as name, description and color and view the promoters as a custom track in the [UCSC Genome Browser](http://genome.ucsc.edu).

+ **Get DNA Sequences** for all found promoters. In addition to the promoter sequences given by their genomic coordinates, a maximum of 500 extra nucleotides can be added to each the 5' and 300 nucleotides to the 3' end of each individual promoter sequence.

+ **Motif Discovery**: Perform basic motif discovery on the resulting promoter sequences using the [MEME motif discovery tool](http://meme-suite.org/). The promoter sequences can be padded with a maximum of 500 extra nucleotides on the 5' and 300 on the 3' ends. The MEME job will be sent via email if the user inputs a valid email address.

    !!! <i class="fa fa-exclamation-circle"></i> **Note:**  
    !!!
    !!! The online version of MEME only accepts a maximum of 1,000 sequences which in total must not exceed 60,000 nucleotides.  All sequences must be longer than 8 nucleotides.

