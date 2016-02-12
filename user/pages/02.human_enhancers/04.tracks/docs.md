---
title: Predefined Tracks
taxonomy:
    category: docs
---



### This section describes the predefined [tracks page](http://slidebase.binf.ku.dk/human_enhancers/presets) for enhancers. 
 
Using statistical methods, we have defined several enhancer tracks used in [Andersson et al.](http://dx.doi.org/doi:10.1038/nature12787) Most track sets are defined in the [BED format ](https://genome.ucsc.edu/FAQ/FAQformat.html#format1) and can be downloaded.  These include:

* **Extensive enhancers (section 1):** 
    - ubiquitous enhancers expressed over the entire set of cell facets; 
    - ubiquitous enhancers expressed over the entire set of tissue(organs) facets; 
    - TSS-enhancer associations (RefSeq promoters only); 
    - permissive and robust enhancer sets as defined in Andersson et al. 
    
    !!! <i class="fa fa-exclamation-circle"></i> **Note:**
    !!! SlideBase searches and information are only associated with the robust enhancer set.

* **Enhancers specifically expressed** in each individual facet from the cell or the tissue (organ) facet sets **(sections 2 and 3)**

The extensive and specifically expressed enhancer sets (sections 1, 2 and 3) can be marked and downloaded or viewed in the [UCSC Genome Browser](https://genome.ucsc.edu/) individually or in combination by selecting the desired sets. Each predicted enhancer in these sections is described in BED12 format with two blocks denoting the merged regions of transcription initiation on the minus and plus strands. The thickStart and thickEnd columns denote the inferred mid position. The score column gives the maximum pooled expression of TCs used to construct each bidirectional loci.

* **Other enhancer expression tracks (section 4):**
    - Enhancers expressed in all facets (both cell and organ);
    - Enhancers that are positively differential expressed in each facet against any other facet
    - Binary matrix of enhancer usage (significant enhancer expression compared to random regions; 1 means used) across all considered FANTOM libraries
    - Expression (TPM and RLE normalized) matrix of enhancers across all considered FANTOM libraries

<br>
* ** Enhancer - FANTOM Robust Promoter associations (section 5):** enhancer-promoter associations are obtained by correlating (Pearson) enhancer-promoter pairs within 500 kbases over cell type and organ facets and filtered by an adjusted correlation pvalue: FDR < 10<sup>-5</sup>. The enhancer-promoter associations are computed between enhancers and all FANTOM robust promoters.
    !!! <i class="fa fa-exclamation-circle"></i> **Note:**
    !!! The Enhancer - FANTOM Robust promoter associations tracks from section 5 are different from the TSS-enhancer (RefSeq promoters only) track from section 1
    