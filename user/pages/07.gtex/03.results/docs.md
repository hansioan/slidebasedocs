---
title: Gene Results
taxonomy:
    category: docs
---

### This section describes the [viewer page](http://slidebase.binf.ku.dk/gtex/results) for GTEx V6 genes. 

Based on the expression constraints, the number of resulting genes will differ. After selecting the search options from the [search page](http://slidebase.binf.ku.dk/docs/gtex/selector) and clicking the **See Detailed Results >>**  (or the smaller **"view"** popup) link, the user will be directed to the viewer page. 

The viewer page displays detailed information about the resulting genes and allows the user to perform actions on the resulting set such as viewing genes in the GTEx Gene Page and GTEx eQTL Browser.  The complete set of gene information and actions are displayed below.

The selected genes are shown on the list to the left as Ensembl-RefSeq name pairs. A maximum number of 50 Ensembl-RefSeq name pairs are displayed on each page. You can use the **First**, **Prev**, **Next** and **Last** buttons located under the results list and at the bottom of the page to view a different subset. Clicking on an name pair shows information about that individual gene with respect to that individual pair; the information is organised into two sheets (tabs): **Expression Details** for gene expression and **eQTLs** for gene-SNP pairs.

#### Expression Details

There are two sections which describe a probeset-gene result:

- **Annotation details**: describes the Ensembl and RefSeq gene names links to GTEx Gene (e.g. [http://www.gtexportal.org/home/gene/GEN1](http://www.gtexportal.org/home/gene/GEN1) ) Page and [eQTL Browser](http://www.gtexportal.org/home/browseEqtls). 

- **Percentage and expression** levels for a gene measured in all samples.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
! Compared to the FANTOM datasets, the GTEx results page displays less information and offers fewer options. This is because the emphasis was put on selection of genes rather than viewing information. A great deal of information can be viewed in GTEx directly, to which we link for each result obtained.

#### Single Tissue eQTL Data (eQTLs)
This table contains significant gene - SNP pairs (on GTEx portal: "eGene and significant SNP-gene associations based on permutations"). The columns in the table are:
- SNP chromosome 
- SNP position
- SNP id
- distance from SNP to TSS
- Tissue (sample) name

!!!! <i class="fa fa-exclamation-circle"></i> **Info:**
!!!! Download information about the GTEx data used in SlideBase is available [here](../background)