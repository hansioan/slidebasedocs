---
title: Search for genes using sliders 
taxonomy:
    category: docs
---

Based on the expression of individual genes across different samples we have transformed the expression values into percentage values.  We have computed the percentages for each expressed, thus resulting in a set of percentage values for all genes. 

We can use the percentage ranges to filter genes based on their expression across samples. The percentage (%) number for each sample refers to how much of the total expression the gene emits for this particular sample.

For each sample we define a slider with values ranging from 0 to 100 corresponding to gene percentages for a specific sample. A percentage range  **_a – b_**  for a certain sample indicates that we are searching for genes with a minimum percentage value of (at least) **_a_** and a maximum percentage value of (at most) **_b_** for that sample. Each sample slider includes two slider handles, which can be adjusted to set a percentage range (e.g. 0% - 100%, 35% - 77%).  

By default, all samples sliders are set to the 0 - 100 range (at least 0% and at most 100%). In this way, we start off with no constraints on the percentage of expression. The percentage range is shown as **“min”** and **“max”** values. 



!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!! + The sum of all **min** percentage values cannot exceed 100%. 

!!!! <i class="fa fa-exclamation-circle"></i> **Tips:**
!!!! + To limit the "influence" of a specific sample in the overall expression constraints, reduce the **max** value to a lower value.
!!!! + To exclude genes expressed in one or more samples, set both **min** and **max** to 0 for those samples.
!!!! + To search for genes with an exact percentage value in a specific sample set both **min** and **max** to the desired percentage value for that sample. <br>
!!!! + To select the genes with 100% percentage of expression in a certain sample, set both **min** and **max** to 100 for that sample.



The example image below shows the slider corresponding to microarray gene expression in the liver. 

![](/images/biogps/sliders-ex0.png)

The percentage range values can be adjusted by:

* **Directly typing the number** in the **min** and **max** input boxes;

* **Moving the blue slider handles** at either edge along the slider bar;

* **Clicking the arrows** buttons to increase/decrease the percentage. The **"<"** and **">"** buttons change the percentage with increments of 0.5%. The **"<<"** and **">>"** buttons change the percentage with increments of 5%.

The number of genes that satisfy the selected constraint(s) are shown in the left upper corner or in a popup window if you are changing expression constraints lower in the page (see examples below).

#### Examples
The examples below showcase the BioGPS gene expression selector. The number of genes resulting only depends on expression constraints defined by sample percentage values.

##### Example 1: 
**  Finding genes mostly expressed in the liver **

![](/images/biogps/sliders-ex1-1.png)

We move the lower bound slider ("min") handle to 80%. This means that at least 80% of the expression must come from the liver sample. The results show that 35 genes satisfy this criterion. Clicking “View >>” will show this set of genes.

![](/images/biogps/sliders-ex1-2.png)

##### Example 2: 

** Finding genes where around half the signal comes from the liver**

![](/images/biogps/sliders-ex2.png)

Here, both left and right slider handles are moved to 45% and 55%. This means that at least 45% and at most 55% of the signal has to come from this sample, and the rest comes from other samples. This results in 38 genes. 

##### Example 3: 

** Finding genes that have almost no expression signal in the liver **
!!! <i class="fa fa-exclamation-circle"></i> **Note:**
!!! The expression values for the BioGPS U133 Gene Atlas are all strictly larger than zero and because of this, if we set both the "min" and "max" percentage values to 0 we would not get any results. Thus, we can set "min"  to 0% and "max" to a value small enough but not zero, which in this case will be 0.10%

![](/images/biogps/sliders-ex-3_v1.png)

To only select genes that have almost no signal from this sample, we move both slider handles to 0%. This results in 824 genes.

##### Example 4: 

** Finding genes that are co-expressed in liver and fetal liver**

![](/images/biogps/sliders-ex4.png)

Here, we have used two sliders in combination, requiring that 25% of signal has to arise from liver AND fetal liver at the same time. This results in 23 genes. 

#### Results panel

The **Results** panel is located in the top left corner of the selector page and contains options for constraining and sorting the results along with the **Number of Hits** found by SlideBase. The number of hits will update in real time as search options are changed. In addition the panel also contains **See Detailed Results >> ** button which will take the user to the [results page](http://slidebase.binf.ku.dk/docs/biogps_atlas/results). 

Based on the expression values we may choose to constrain the results or not. This can be done by selecting one of the two options from the **Show Results That Match** dropdown.

In addition to expression constraining, there is also the option of sorting the results based on a chosen sample. This can be done by choosing the desired sample from the dropdown menu **Sort Results By**.  To sort ascending or descending based on the sample expression, select the option from the dropdown menu **Sort Type**.  By default the results are not sorted and this is shown by the option "Do Not Sort" in the **Sort Results By** dropdown menu.

![](/images/biogps/sliders-ex1-2.png)

#### Disabling and resetting

The sample percentage values can be disabled by clicking the **Disable** button located in the header the slider container. Disabling the percentage of expression for samples implies that their expression values will not be taken into account when searching for genes.


The percentage values can be reset by clicking on the **Reset** button located in the slider set container header. Resetting the expression percentage values will trigger the **min** and **max** values for all sample percentage values to become 0% and 100% (all **min** = 0%, all **max** = 100%).

