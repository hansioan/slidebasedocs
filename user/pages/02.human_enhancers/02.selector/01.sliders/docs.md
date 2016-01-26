---
title: Search for enhancers using sliders 
taxonomy:
    category: docs
---

Based on the expression of individual enhancers across all samples (cell type and tissue/organ) we have transformed the expression values into percentage values.  We have computed the percentages for each enhancer across the cell type and tissue sets independently of each other, thus resulting in two sets of percentage values for all enhancers. 

We can use the percentage ranges to filter enhancers based on their expression across samples. The percentage (%) number for each cell type/tissue refers to how much of the total expression (normalized CAGE tag counts from all cells and tissues) the enhancer emits for this particular cell type/tissue.  

For each sample (cell type or tissue) we define a slider with values ranging from 0 to 100 corresponding to enhancer percentages for a specific sample. A percentage range  **_a – b_**  for a certain sample indicates that we are searching for enhancers with a minimum percentage value of (at least) **_a_** and a maximum percentage value of (at most) **_b_** for that sample. Each sample slider includes two slider handles, which can be adjusted to set a percentage range (e.g. 0% - 100%, 35% - 77%).  

By default, all samples sliders are set to the 0 - 100 range (at least 0% and at most 100%). In this way, we start off with no constraints on the percentage of expression. The percentage range is shown as **“min”** and **“max”** values. 



>>>>> In each of the two samples sets (cells and tissues), the sum of all **min** percentage values cannot exceed 100%. 

<br>

>>>>>> To limit the "influence" of a specific sample in the overall expression constraints, reduce the **max** value to a lower value. <br>
    To exclude enhancers expressed in one or more samples, set both **min** and **max** to 0 for those samples.<br>
    To search for enhancers with an exact percentage value in a specific sample set both **min** and **max** to the desired percentage value for that sample. <br>
    To select the enhancers with 100% percentage of expression in a certain sample, set both **min** and **max** to 100 for that sample.



The example image below shows the slider corresponding to CAGE enhancer expression in the large intestine. 

>>>>> Insert image (see Albin docs)

The percentage range values can be adjusted by:

* **Directly typing the number** in the **min** and **max** input boxes;

* **Moving the blue slider handles** at either edge along the slider bar;

* **Clicking the arrows** buttons on the ends of the slider bar to increase/decrease the percentage. The **"<"** and **">"** buttons change the percentage with increments of 0.5%. The **"<<"** and **">>"** buttons change the percentage with increments of 5%.


