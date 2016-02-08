---
title: Search for genes using sliders 
taxonomy:
    category: docs
---

The selector page contains two types of sliders. 
+ **RNA sliders**: select genes based on RNA expression levels measured with RNA-Seq
+ **Protein sliders:** select genes based on protein abundance from antibody-based measurements

##### RNA sliders
Based on the RNA expression of individual genes across all samples we have transformed the RNA expression values into percentage values.  We have computed the percentages for each gene across all samples, thus resulting a set of percentage values for all genes. 

We can use the percentage ranges to filter genes based on their expression across samples. The percentage (%) number for each sample refers to how much of the total expression (Fragments Per Kilobase of transcript per Million mapped reads FPKM) the gene emits for this particular sample.  

For each sample we define a slider with values ranging from 0 to 100 corresponding to gene percentages for a specific sample. A percentage range  **_a – b_**  for a certain sample indicates that we are searching for genes with a minimum percentage value of (at least) **_a_** and a maximum percentage value of (at most) **_b_** for that sample. Each sample slider includes two slider handles, which can be adjusted to set a percentage range (e.g. 0% - 100%, 35% - 77%).  

By default, all samples sliders are set to the 0 - 100 range (at least 0% and at most 100%). In this way, we start off with no constraints on the percentage of expression. The percentage range is shown as **“min”** and **“max”** values. 



!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!! + For all RNA slider samples, the sum of all **min** percentage values cannot exceed 100%. 

!!!! <i class="fa fa-exclamation-circle"></i> **Tips:**
!!!! + To limit the "influence" of a specific sample in the overall expression constraints, reduce the **max** value to a lower value.
!!!! + To exclude genes expressed in one or more samples, set both **min** and **max** to 0 for those samples.
!!!! + To search for genes with an exact percentage value in a specific sample set both **min** and **max** to the desired percentage value for that sample. <br>
!!!! + To select the genes with 100% percentage of expression in a certain sample, set both **min** and **max** to 100 for that sample.

The example image below shows the slider corresponding to RNA-Seq gene expression in the cerebral cortex. 

![](/images/protein_atlas/sliders-ex0-1.png)

The percentage range values can be adjusted by:

* **Directly typing the number** in the **min** and **max** input boxes;

* **Moving the round blue slider handles** at either edge along the slider bar;

* **Clicking the arrows** buttons on the ends of the slider bar to increase/decrease the percentage. The **"<"** and **">"** buttons change the percentage with increments of 0.5%. The **"<<"** and **">>"** buttons change the percentage with increments of 5%.

The number of genes that satisfy the selected constraint(s) are shown in the left upper corner or in a popup window if you are changing expression constraints lower in the page (see examples below).

##### Protein sliders
Based on the protein abundance levels of individual genes across all samples we have defined protein sliders having four levels of protein abundance: **None (Not detected)**, **Low**, **Medium** and **High**.

The protein abundance levels are measured from the same samples as RNAs and from an additional numbers of samples for which there are no RNA levels. Sliders have been defined for both the common samples and the protein only samples. The common sliders are shown in paralel for RNA and protein sliders while the protein only sample sliders are shown at the end. Similar to the RNA sliders, we have a ranged value for protein levels as well. The range is defined by the position of the protein slider handles. The default range is defined to include all protein levels (from not detected (None) to High).

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!! + Unlike the RNA sliders, there is no limitation on how the protein sliders can be used

The example image below shows the slider corresponding to RNA-Seq gene expression in the cerebral cortex. 

![](/images/protein_atlas/sliders-ex0-2.png)

The protein levels can be adjusted by moving the blue square slider handles in one of the four positions.


#### Examples
The examples below showcase the gene selectors. The number of genes resulting only on RNA expression and/or protein level constraints defined by sample sliders.

##### Example 1: 
** Finding genes almost exclusively expressed in the cerebral cortex **

![](/images/protein_atlas/sliders-ex1-1.png)

We move the RNA lower bound slider ("min") handle to 90%. This means that at least 90% of all RNA-Seq signals must come from the cerebral cortex sample. The results show that 90 genes satisfy this criterion. Clicking “View >>” will show this set of genes.

![](/images/protein_atlas/sliders-ex1-2.png)

##### Example 2: 

** Finding genes where around half the RNA signal comes from the cerebral cortex **

![](/images/protein_atlas/sliders-ex2.png)

Here, both left and right RNA slider handles are moved to 45% and 55%. This means that at least 45% and at most 55% of the RNA signal has to come from this sample, and the rest comes from other samples. This results in 141 genes. 

##### Example 3: 

** Finding genes that have no RNA expression signal in the cerebral cortex **

![](/images/protein_atlas/sliders-ex3.png)

To only select genes that have no signal from this sample, we move both slider handles to 0%. This gives as many as 3,047 genes, meaning that many genes are not present at all in this sample. This type of selection makes the most sense when combining sliders (see next example)

##### Example 4: 

** Finding genes that have high RNA expression and high protein abundance levels the cerebral cortex **

![](/images/protein_atlas/sliders-ex4.png)

Here, we have used two sliders in combination, requiring that 90% of RNA signal has to arise from the cerebral cortex and also have a "High" protein abundance level in the same sample. This results in 13 genes. 


#### Combining RNA and protein levels and the Results panel

The **Results** panel is located in the top left corner of the selector page and contains options for constraining and sorting the results along with the **Number of Hits** found by SlideBase. The number of hits will update in real time as search options are changed. In addition the panel also contains **See Detailed Results >> ** button which will take the user to the [results page](http://slidebase.binf.ku.dk/docs/protein_atlas/results). 

As seen in example 4 it is possible to combine sliders that describe both RNA and protein abundance levels if relevant. Given this, you can choose how to constrain the levels from the two sample sets by selecting options from dropdown menu labeled **Show Results That Match**, shown in the **Results** panel:

+ **RNA AND Protein Constraints:** constraints from **both the RNA and protein** sample sets so that the resulting gene set is a combination of RNA **AND** protein constrains (genes that follow both the RNA AND the protein constraints will be returned)

+ **RNA OR Protein Constraints:** constraints from **either the RNA and protein** sample sets so that the resulting gene set is a combination of RNA **OR** protein constrains (genes that follow both the RNA OR the protein constraints will be returned)

+ **RNA Constrains Only:** only apply the constraints set by the RNA expression and ignore protein levels when searching

+ **Protein Constraints Only:** apply the constraints set by the protein levels and ignore RNA expression when searching

+ **Ignore Constraints:**  as the name specifies, do not take into account any sample constraints 

In addition to constraining the search to specific samples, there is also the option of sorting the results based on a chosen sample (from either RNA  or protein samples). This can be done by choosing the desired sample from the dropdown menu **Sort Results By**.  To sort ascending or descending based on the sample levels, select the option from the dropdown menu **Sort Type**.  By default the results are not sorted and this is shown by the option "Do Not Sort" in the **Sort Results By** dropdown menu.

![](/images/protein_atlas/sliders-ex1-2.png)

#### Disabling and resetting

The RNA and protein levels can be disabled by clicking the **Disable** button located in the header of both slider set containers. Disabling the values for either or both RNA and protein samples implies that their values will not be taken into account when searching for genes.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! SlideBase will only constrain on the enabled sample sets. If, for example, only the RNA sliders are disabled, the value of the **Show Results That Match** dropdown will be **Protein Constraints Only**. If both RNA and protein sliders are disabled the selected dropdown value will be **Ignore Constraints**.   

The RNA and protein levels can be reset by clicking on the **Reset** button located in the header of both slider set containers. Resetting the values for RNA samples will trigger the **min** and **max** values for  all RNA percentage values to become 0% and 100% (all **min** = 0%, all **max** = 100%). Resetting the values for protein samples will trigger the **min** and **max** values for all protein to become None (Not detected) and High (all **min** = None, all **max** = High). 

