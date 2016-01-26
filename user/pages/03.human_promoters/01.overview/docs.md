---
title: Overview
taxonomy:
    category: docs
---

1. Background research

The FANTOM5 consortium have extracted RNA transcripts from a multitude of different primary cells and tissues using the CAGE experiment (short for Cap Analysis of Gene Expression). As a result, mappings of transcription start sites and their usage in human primary cells and post-mortem tissues were produced in order to construct a comprehensive overview of gene expression across the human body.
This has been done using CAGE and single-molecule sequencing. The result is a unique gene expression profile atlas, focused specifically on core promoter utilization. CAGE has advantages over RNA-seq or microarrays for this purpose, because it permits separate analysis of multiple promoters linked to the same gene. In consequence, for each promoter we have a measure of expression within each primary cell and tissue and based on the expression levels a promoter can be specific to a set of primary cells and tissues or can be broadly expressed. Expression levels are measured in CAGE tags (simple or normalized). The expression levels used in PrESSTo are measured in TPM (tags per million). In addition, the mapping and annotation process has found promoters associated with known genes as well as anonymous (or novel) promoters, which are not close to known genes.


In PrESSTo we have simplified the samples by aggregating anatomically/functionally similar cells and tissues into “facets”. Examples of cell facets are: neurons, T cells or monocytes; example of tissue facets are: brain, liver or heart tissue.


2. Defining sliders and searching (the search page)

Based on the expression of individual promoters and enhancers across all cells and all tissues we have transformed the expression values into percentage values. Given this we can define sliders from 0 to 100% which we can use to filter enhancers and promoters based on their expression across a set of samples.
For instance, moving the liver slider to 10% and the intestine slider to 50% results in all promoters where at least 10% of CAGE tags are from liver at at least 50% are from intestine.  
In addition we can also set location constraints based on the genomic location of promoters and enhancers to further refine our search. The location search offers the option to search near known genes with default values of 100K bp up and downstream gene boundaries.


2.1 Slider Search Details:
The percentage (%) number for each cell type/tissue refers to how much of the total expression (normalized CAGE tag counts from all cells and tissues) the promoter emits for this particular cell type/tissue. The percentage number is a "lowest bound" value: only the promoters that have higher percentage of expression than the set value for the cell type/tissue will be returned.
The percentage numbers for each cell/tissue can be set in three ways:

§  Directly typing the number in the input box;

§  Moving the slider along the slider bar;

§  Clicking the arrows buttons on the ends of the slider bar to increase/decrease the percentage. The "<" and ">" buttons change the percentage with increments of 0.5%. The "<<" and ">>" buttons change the percentage with increments of 5%.

The primary cell/tissue percentage values can be disabled by clicking the "Disable" button. Disabling the percentage values for either or both cells and tissues implies that their percentage numbers will not be taken into account when searching for promoters (they are all zero % ).
By clicking the "Reset" buttons , all primary cells and/or tissue percentage values will be reset to zero %.
The total value of all non-zero primary cells/tissue percentage cannot exceed 100%. The remaining percentage available is shown above the "Reset" button.

2.2 Location search details:
There are two ways to set the location search information:
Directly setting the specific sites. You can choose all or a specific chromosome from the "Chromosome" selectors, and then input a starting site and an ending site (inclusive) and the strand. This will be the searching range. When choosing a chromosome, the starting site will contain the value 1, the ending site will contain the size of the chromosome and the strand value will represent both the plus and the minus strand.
Searching for interested genes. You can type a gene name (refseq gene ID) in the "Gene" box, and select the desired gene based on it's name, location and (possibly multiple) UCSC transcripts. After selecting a gene, the starting and ending sites will become the Transcription Start Site and Transcription End Site respectively of the particular gene. By default the gene coordinates are expanded upstream and downstream by 100 kilobases as shown in the "Up and Down Stream" boxes. The extension coordinates can be adjusted by setting the "Up and Down Stream" base pair numbers. The gene strand is provided by the "Strand" box.
When selecting from the two types of location search (basic or gene-based), its corresponding search parameter area will be displayed with a light green background while the other option area will be displayed in gray.
To move from gene-based search to the basic search (remove/reset gene options) double click the left box containing the basic search components, namely chromosome, start-site and end-site and strand, or change the values in either of these components.
Note that moving from the gene-based search to the basic location search by double-clicking will trigger all the search parameters to reset to the initial location search, which spans across all chromosomes.
The "Sort by" selector on the right-most side informs on which of the cells’ or organ's expression value the result will be sorted by. The sort type is descending.
The location search can be disabled by clicking the "Disable" button on the top-right corner. Disabling the location search implies that the search will be conducted among all the chromosomes.

2.3. Result Options

The number of resulting promoters will be automatically updated after each change in sliders or location values. The number is shown in the box on the right with the caption “number of hits”. In addition, the cell and tissue slider filters can be changed to the following:

§  Cell AND Organ (Tissue) Constraints: constraints from both the cell and tissue slider sets so that the resulting promoter set is a combination of cell AND tissue constrains (promoters that follow both the cell AND the tissue constraints will be returned)

§  Cell OR Organ (Tissue) Constraints: constraints from either the cell and tissue slider sets so that the resulting promoter set is a combination of cell OR tissue constrains (promoters that follow either the cell OR the tissue constraints will be returned)

§  Cell Constrains Only: only apply the constraints set by the cells sliders and ignore tissue sliders when searching

§  Organ(Tissue) Constraints Only: apply the constraints set by the cells sliders and ignore tissue sliders when searching

By clicking the “See Detailed Results >>” link the user will be directed the viewer page displaying detailed information about the resulting promoters.



3. View Resulting Promoters (the viewer page)

Based on the expression and genomic location constraints, the number of resulting promoters will differ. After selecting your search options from the search page click the “See Detailed Results >>” link to go to the viewer page. 

The viewer page displays detailed information about the resulting promoters and allows the user to perform actions on the resulting set such as downloading and viewing in genome browsers.  The complete set of promoter information and actions is displayed below.

Your selected promoters are shown on the list to the left. A maximum number of 50 promoters are displayed on each page. You can use the "First", "Prev", "Next" and "Last" buttons at the bottom-left side of the page to view a different subset. Clicking on a promoter shows information about that individual promoter:


§  Promoter Annotation Details: table that shows promoter description and whether the promoter is associated with a known gene.  Values of NA represent no association or missing while other values describe or refer to associated gene, protein or sample resources.

§  Percentage and Expression Tables: percentage and expression tables for primary cells (facets), organs (facets) and libraries (sample level expression). The sample wise expression table contains links to SSTAR  which holds detailed information about each sample. Most table columns can be sorted by clicking on the table column header.


§  View promoter in UCSC Genome Browser: Input UCSC track information such as name, description and color and view the individual promoter as a track in the UCSC Genome Browser.


§  View promoter in ZENBU Genome Browser: View promoter information similar to UCSC in the ZENBU Genome Browser from FANTOM.  A special feature in ZENBU is the option to view expression levels

§  View in FANTOM5 Explorer: Promoters associated with known genes can be visualized in the FANTOM5 explorer in terms of expression and as part of a hierarchical differentiation tree.


§  View Overlaps: View promoter-enhancer and promoter-SNP overlaps. A promoter-enhancer overlap occurs when the distance from a promoter summit to an enhancer center is within 500 kbp and the Pearson correlation adjusted pvalue is: FDR < 10-5. More about promoter summits and enhancer centers in the publications listed in section 4 of this documentation. If a promoter-enhancer overlap exists, the enhancer can be further inspected by clicking on the enhancer annotation and going to the PrESSTo human enhancers selector. A promoter-SNP overlap occurs when a SNP  is located within 300 bp upstream or 100 bp downstream the promoter summit. If an promoter-SNP overlap exists the SNP can be further inspected by clicking on the SNP id.


Based on the selection parameters from the slider tool, a number of promoters can be found. Given the resulting promoters the following options are available:

§  Download all found promoters as BED files.

§  View all found promoters in the UCSC Genome Browser: Input UCSC track information such as name, description and color and view the promoters as a custom track in the UCSC Genome Browser.

§  Get DNA Sequences for all found promoters. In addition to the enhancer sequences given by their genomic coordinates, a total of 600 extra nucleotides can be added to the 5' and/or 3' end of each individual sequence.

§  Motif Discovery: Perform basic motif discovery on the resulting promoter sequences using the MEME motif discovery tool. The promoter sequences can be padded with a total of 600 extra nucleotides at the 5’ and/or 3’ end. The MEME job will be sent via email if the user inputs a valid email address. Note:  The online version of MEME only accepts a maximum of 1,000 sequences which in total must not exceed 60,000 nucleotides.  All sequences must be longer than 8 nucleotides.  In addition the maximum upstream and downstream extensions must not exceed 600 nucleotides.



4. Additional information and citation

For more details on the enhancer tracks or any other research aspects behind enhancers or promoters please consult the following publications:

§  The FANTOM 5 Consortium and the RIKEN PMI and CLST (DGT), Nature 507, 462–470, doi:10.1038/nature13182  *

§  Andersson et al, Nature 507, 455–461, doi:10.1038/nature12787 *

§  Arner et al, Science vol. 347,1010-1014, doi: 10.1126/science.1259418


* Papers to cite if you are using PrESSTo