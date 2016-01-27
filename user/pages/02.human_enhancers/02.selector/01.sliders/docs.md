---
title: Search for enhancers using sliders 
taxonomy:
    category: docs
---

Based on the expression of individual enhancers across all samples (cell type and tissue/organ) we have transformed the expression values into percentage values.  We have computed the percentages for each enhancer across the cell type and tissue sets independently of each other, thus resulting in two sets of percentage values for all enhancers. 

We can use the percentage ranges to filter enhancers based on their expression across samples. The percentage (%) number for each cell type/tissue refers to how much of the total expression (normalized CAGE tag counts from all cells and tissues) the enhancer emits for this particular cell type/tissue.  

For each sample (cell type or tissue) we define a slider with values ranging from 0 to 100 corresponding to enhancer percentages for a specific sample. A percentage range  **_a – b_**  for a certain sample indicates that we are searching for enhancers with a minimum percentage value of (at least) **_a_** and a maximum percentage value of (at most) **_b_** for that sample. Each sample slider includes two slider handles, which can be adjusted to set a percentage range (e.g. 0% - 100%, 35% - 77%).  

By default, all samples sliders are set to the 0 - 100 range (at least 0% and at most 100%). In this way, we start off with no constraints on the percentage of expression. The percentage range is shown as **“min”** and **“max”** values. 



!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!! + In each of the two samples sets (cells and tissues), the sum of all **min** percentage values cannot exceed 100%. 

!!!! <i class="fa fa-exclamation-circle"></i> **Tips:**
!!!! + To limit the "influence" of a specific sample in the overall expression constraints, reduce the **max** value to a lower value.
!!!! + To exclude enhancers expressed in one or more samples, set both **min** and **max** to 0 for those samples.
!!!! + To search for enhancers with an exact percentage value in a specific sample set both **min** and **max** to the desired percentage value for that sample. <br>
!!!! + To select the enhancers with 100% percentage of expression in a certain sample, set both **min** and **max** to 100 for that sample.



The example image below shows the slider corresponding to CAGE enhancer expression in the large intestine. 

!!!     Insert image (see Albin docs)

The percentage range values can be adjusted by:

* **Directly typing the number** in the **min** and **max** input boxes;

* **Moving the blue slider handles** at either edge along the slider bar;

* **Clicking the arrows** buttons on the ends of the slider bar to increase/decrease the percentage. The **"<"** and **">"** buttons change the percentage with increments of 0.5%. The **"<<"** and **">>"** buttons change the percentage with increments of 5%.

The number of enhancers that satisfy the selected constraint(s) are shown in the left upper corner or in a popup window if you are changing expression constraints lower in the page (see examples below).


##### Example 1: 
** _ Finding enhancers almost exclusively expressed in the large intestine _ **

!!! Slider image ask Albin

We move the lower bound slider ("min") handle to 90%. This means that at least 90% of all CAGE signals must come from the large intestine sample. The pop-up on the left shows that 19 enhancers satisfy this criterion. Clicking “View >>” will show this set of enhancers. 

##### Example 2: 

** _Finding enhancers where around half the signal comes from the large intestine_ **

!!! Slider image ask Albin

Here, both left and right slider handles are moved to 45% and 55%. This means that at least 45% and at most 55% of the signal has to come from this sample, and the rest comes from other samples. This results in 66 enhancers. 

##### Example 3: 

** _Finding enhancers that have no expression signal in the large intestine_ **

!!! Slider image ask Albin

To only select enhancers that have no signal from this sample, we move both slider handles to 0%. This gives as many as 22.266 enhancers, meaning that many enhancers are not present at all in this sample. This type of selection makes the most sense when combining sliders for different samples (see next example)

##### Example 4: 

** _Finding enhancers that are co-expressed in small and large intestine_ **

!!! Slider image ask Albin

Here, we have used two sliders in combination, requiring that 25% of signal has to arise from large AND small intestine at the same time. This results in 35 enhancers. 

##### Example 5: 

** _Finding enhancers that are co-expressed in small and large intestine but not expressed in blood vessels_ **

!!! Slider image ask Albin

In this example, we have added a negative constraint to the last example, by setting the maximal expression in the blood vessel sample to zero. This reduces the number of enhancers to 25. 


#### Combining cell and organ expression and the Results panel

The **Results** panel is located in the top left corner of the selector page and contains options for constraining and sorting the results along with the **Number of Hits** found by SlideBase. The number of hits will update in real time as search options are changed. In addition the panel also contains **See Detailed Results >> ** button which will take the user to the [results page](http://slidebase.binf.ku.dk/docs/human_enhancers/results). 

Note that while the above examples have only been using organ expression, it is possible to combine sliders that describe primary cells and organ expression if relevant. Given this, you can choose how to constrain the expression values from the two sample sets by selecting options from dropdown menu labeled **Show Results That Match**, shown in the **Results** panel:

+ **Cell AND Organ (Tissue) Constraints:** constraints from **both the cell and tissue** sample sets so that the resulting enhancer set is a combination of cell **AND** tissue constrains (enhancers that follow both the cell AND the tissue constraints will be returned)

+ **Cell OR Organ (Tissue) Constraints:** constraints from **either the cell or tissue** sample sets so that the resulting enhancer set is a combination of cell **OR** tissue constrains (enhancers that follow either the cell OR the tissue constraints will be returned)

+ **Cell Constrains Only:** only apply the constraints set by the cells expression and ignore tissue expression when searching

+ **Organ(Tissue) Constraints Only:** apply the constraints set by the cells expression and ignore tissue expression when searching

+ **Ignore Sample Constraints:**  as the name specifies, do not take into account any expression constraints 

In addition to constraining the search to specific samples, there is also the option of sorting the results based on a chosen sample (cell or tissue). This can be done by choosing the desired sample from the dropdown menu **Sort Results By**.  To sort ascending or descending based on the sample expression, select the option from the dropdown menu **Sort Type**.  By default the results are not sorted and this is shown by the option "Do Not Sort" in the **Sort Results By** dropdown menu.

#### Disabling and resetting

The primary cell/tissue percentage values can be disabled by clicking the **Disable** button located in the header of both slider set containers. Disabling the percentage values for either or both cells and tissues implies that their percentage numbers will not be taken into account when searching for enhancers.

!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!!
!!! SlideBase will only constrain on the enabled sample sets. If, for example, only the primary cells sliders are disabled, the value of the **Show Results That Match** dropdown will be **Organ Constraints Only**. If both cells and tissue sliders are disabled the selected dropdown value will be **Ignore Sample Constraints**.   

The percentage values can be reset by clicking on the **Reset** button located in the header of both slider set containers. Resetting the expression percentage values for either or both cells and tissues will trigger the **min** and **max** values for  all primary cells and/or tissue percentage values to become 0% and 100% (all **min** = 0%, all **max** = 100%).

