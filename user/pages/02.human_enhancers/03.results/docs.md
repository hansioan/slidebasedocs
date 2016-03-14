---
title: Enhancer Results
taxonomy:
    category: docs
---

### This section describes the [viewer page](http://slidebase.binf.ku.dk/human_enhancers/results) for enhancers. 

Based on the expression and/or genomic location constraints, the number of resulting enhancers will differ. After selecting your search options from the [search page](http://slidebase.binf.ku.dk/docs/human_enhancers/selector) and clicking the **See Detailed Results >>**  (or the smaller **"view"** popup link) link, the user will be directed to the viewer page. 

The viewer page displays detailed information about the resulting enhancers and allows the user to perform actions on the resulting set such as downloading and viewing in genome browsers.  The complete set of enhancer information and actions are displayed below.

Your selected enhancers are shown on the list to the left. A maximum number of 50 enhancers are displayed on each page. You can use the **First**, **Prev**, **Next** and **Last** buttons located under the enhancer list and at the bottom of the page to view a different subset. Clicking on an enhancer shows information about that individual enhancer as three different sheets (tabs): **CAGE Details** for expression, **Browse** for genome browser views and **View Overlaps** for basal overlaps and correlations with proximal genomic entities. It is also possible to analyze all selected enhancers (see below). 


### Single enhancer information

This section describes the vizualization / analyses / overlaps for a single enhancer. Each option presented below corresponds to one of the sheets (tabs) available on the viewer page. 

##### CAGE Details
This view shows the enhancer expression. Specifically, percentage and expression tables for primary cells (facets), organs (facets) and libraries (actual sample level expression for all the samples that make up each facet) are available. 

For the primary cells and organ facets the tables indicate whether the enhancer is significantly overrepresented in a specific primary cell or organ facet based on statistical tests described in [Andersson et al.](http://dx.doi.org/doi:10.1038/nature12787) The indication of over-represented is given by red percentage bars as opposed to light-blue bars for non over-represented. The sample wise expression table contains links to [SSTAR](http://fantom.gsc.riken.jp/5/sstar/) which holds detailed information about each sample. Most table columns can be sorted by clicking on the table column header.

##### Browse
This enables the creation of a custom track of your selected enhancers in either the [UCSC Genome Browser](http://genome.ucsc.edu/) or the [ZENBU Genome Browser](http://fantom.gsc.riken.jp/zenbu/).  The UCSC browser has the option of coloring tracks, and houses a larger amount of different data types. ZENBU, on the other hand, has the advantage of showing actual expression levels of CAGE data with advanced mouse-over functions. 


##### View Overlaps
This shows predicted target promoter(s) of the enhancer, and SNP overlaps.  Enhancer-promoter pairs are predicted based on genomic distance and CAGE co-expression, expressed as Pearson’s correlation tests. An enhancer-promoter prediction is shown when the distance from an enhancer center to a TSS summit is within 500 kbp and the Pearson correlation adjusted P-value (FDR) is < 10<sup>-5</sup> (as in [Andersson et al.](http://dx.doi.org/doi:10.1038/nature12787) ). If an enhancer-promoter overlap exists, the TSS can be further inspected by clicking on the promoter annotation and going to SlideBase [promoter/TSS results page](http://slidebase.binf.ku.dk/docs/human_promoters/results) for that promoter. 

An enhancer-SNP overlap occurs when the distance from an enhancer center and a SNP location is within 200 bp.  If an enhancer-SNP overlap exists the SNP can be further inspected by clicking on the SNP id.


### Multiple enhancer information

**Visualization/analyses of multiple selected enhancers**

Instead of selecting a single enhancer, a number of analyses options are available for the whole set of resulting enhancers, shown above the enhancer list:



+ **Download all** found enhancers as BED files.

+ **View all** found enhancers in the UCSC Genome Browser: Input UCSC track information such as name, description and color and view the enhancers as a custom track in the [UCSC Genome Browser](http://genome.ucsc.edu).

+ **Get DNA Sequences** for all found enhancers. In addition to the enhancer sequences given by their genomic coordinates, a maximum of 400 extra nucleotides can be added to each the 5' and/or 3' end of each individual enhancer sequence.

+ **Motif Discovery**: Perform basic motif discovery on the resulting enhancer sequences using the [MEME motif discovery tool](http://meme-suite.org/). The enhancer sequences can be padded with a maximum of 400 extra nucleotides on each of the 5' and/or 3' ends. The MEME job will be sent via email if the user inputs a valid email address.

    !!! <i class="fa fa-exclamation-circle"></i> **Note:**  
    !!!
    !!! The online version of MEME only accepts a maximum of 1,000 sequences which in total must not exceed 60,000 nucleotides.  All sequences must be longer than 8 nucleotides.


