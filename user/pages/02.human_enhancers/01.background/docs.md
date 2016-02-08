---
title: Background and underlying data
taxonomy:
    category: docs
---


The [FANTOM5 consortium](http://fantom.gsc.riken.jp/) have extracted RNA transcripts from a multitude of different primary cells and tissues using the CAGE experiment (short for Cap Analysis of Gene Expression). As a result, mappings of transcription start sites and their usage in human primary cells and post-mortem tissues were produced in order to construct a comprehensive overview of gene expression across the human body.
This has been done using CAGE and single-molecule sequencing. The result is a unique [gene expression profile atlas](http://dx.doi.org/10.1038/nature13182), focused specifically on core promoter utilization.

Because active enhancer regions are transcribed, we identified a distinct bidirectional CAGE pattern which could predict enhancer regions based on CAGE data not associated with promoters. Because enhancer transcription is a powerful proxy of cell-specific enhancer activity, we could define an [atlas of active, in vivo bidirectionally transcribed enhancers](http://dx.doi.org/doi:10.1038/nature12787) across the human body using the FANTOM5 panel of tissue and primary cell samples. 

Similar to promoters, for each enhancer we have a measure of expression  within each primary cell and tissue, and based on the expression levels an enhancer can be specific to a set of primary cells and organs(tissue samples) or can be broadly (or ubiquitously) expressed. Expression levels are measured in CAGE tags.  The expression levels used in SlideBase are measured in TPM (tags per million).         

In SlideBase we have simplified the samples by aggregating anatomically/functionally similar cells and tissues into "facets", as defined in [Andersson et al](http://www.nature.com/nature/journal/v507/n7493/full/nature12787.html). Examples of cell facets are: neurons, T cells or monocytes; example of tissue facets are: brain, liver or heart tissue.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! If you use this expression data, you should cite:   
!!! - The FANTOM 5 Consortium and the RIKEN PMI and CLST (DGT), Nature 507, 462–470, **doi: 10.1038/nature13182**
!!! - Andersson et al, Nature 507, 455–461, **doi: 10.1038/nature12787**