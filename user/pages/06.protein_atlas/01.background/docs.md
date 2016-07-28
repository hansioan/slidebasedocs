---
title: Background and underlying data
taxonomy:
    category: docs
---

[The human protein atlas](http://www.proteinatlas.org/) is a unique undertaking to profile the protein abundance in tissues  and   cells   using  antibody-based  proteomics  techniques. It  contains information for  a large  majority  of  all  human  protein-coding  genes  regarding  the expression and localization  of the corresponding proteins based on both RNA and protein  data.  

The  tissue  atlas  contains   information  of  44  different  human  tissues and  organs  with  annotation  data  for altogether  83  different  cell  types.  The transcriptomics data provide quantitative data on gene expression levels across the tissues  and  organs,  while  the  antibody-based  protein  profiles  show  the  spatial distribution  at  a  single  cell  level  for  the  corresponding  protein  in  the  various substructures and cell types of the tissues.  In SlideBase, we present the possibility to select genes based on gene expression or protein abundance, or a combination of the two. 

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! If you use this expression data, you should cite:   
!!! - Uhlén M et al, Science 2015 347(6220):1260419, **doi: 10.1038/nbt1210-1248**
!!! - Uhlén M et al, Mol Cell Proteomics. 2005 4(12):1920-32., **doi: 10.1074/mcp.M500279-MCP200**

#### Particularities of SlideBase protein atlas data
The data used in SlideBase is available from [proteinatlas.org](http://www.proteinatlas.org). However, there are some minor differences in the data we select and show in SlideBase. For information on The Human Protein Atlas resources and methods visit the [about](http://www.proteinatlas.org/about) page on proteinatlas.org. 

In SlideBase we currently use data from [version 15](http://v15.proteinatlas.org/about/download) of The Human Protein Atlas. More exactly SlideBase uses the  [Normal tissue data](http://v15.proteinatlas.org/download/normal_tissue.csv.zip) dataset for protein abundance levels and the tissue file of the [RNA gene data](http://v15.proteinatlas.org/download/rna_tissue.csv.zip) dataset for RNA-seq expression levels. 
In order to produce a more intuitive search tool we have simplified our search space by excluding some of the particularities of the Human Protein Atlas data. The changes we made are:

##### Same number of genes

SlideBase uses only genes available in both the RNA expresison and protein abundance datasets; Since the genes in the RNA set include all genes in the protein set, this is equivalent to removing the genes in the RNA levels dataset that are not present in the protein levels dataset. 

##### NA == Low and special protein abundance scores
The protein [scores](http://v15.proteinatlas.org/about/help#12) present of the proteinatlas.org gene information page (i.e. 'PROTEIN EXPRESSION OVERVIEW' table) may contain values which are not in the ("Not detected", "Low", "Medium", "High") levels set. Examples include:

- Cerebral coretex and Colon protein 'scores' for the [GBP1](http://v15.proteinatlas.org/ENSG00000117228-GBP1/tissue) gene in-between the "Not detected" and "Low" levels. These samples have a score of 0.33 rather than a score of 1.0 which denotes a "Low" abundance level or a score of 0.0 which denotes a "Not detected" abundance level.
- Soft tissue and Skin protein 'scores' for the [RUNX1](http://v15.proteinatlas.org/ENSG00000159216-RUNX1/tissue) gene in-between the "Not detected" and "Low" levels. These samples have a score of 0.66 rather than a score of 1.0 which denotes a "Low" abundance level or a score of 0.0 which denotes a "Not detected" abundance level.
- Soft tissue 'score' for the [SCIN](http://v15.proteinatlas.org/ENSG00000006747-SCIN/tissue) gene in-between the "Not detected" and "Low" levels. This sample has a score of 0.99 rather than a score of 1.0 which denotes a "Low" abundance level or a score of 0.0 which denotes a "Not detected" abundance level.
- Adipose tissue 'score' of N/A (not available) for the [SCT](http://v15.proteinatlas.org/ENSG00000070031-SCT/tissue) gene. 

We have simplified the data used in our search so that all scores of 0.33, 0.66 and 0.99 have been given a score of 1.0 ("Low"). Additionally, the N/A values have been replaced with "Not detected". While these special values are not used in our search, we do however display them in our results page and refer to the gene information pages on proteinatlas.org



