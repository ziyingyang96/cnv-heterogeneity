# Copy number variation heterogeneity reveals biological inconsistency in hierarchical cancer classifications

This research combines a large number of copy nymber variants (CNV) profiles and hierarchical NCIt cancer classification system, and introduces several distance/similarity measurements besed on CNV and revealed biological inconsistency between CNV and cancer classification system.

![pipeline_diagram]([https://github.com/ziyingyang96/cnv-signature/blob/main/workflow.png](https://github.com/ziyingyang96/cnv-heterogeneity/blob/main/cnv-heterogeneity-workflow.png))


# Installation
Firstly you have to make sure that you have all dependencies in place. The simplest way to do so, is to use anaconda.

You can create an anaconda environment called cnv_heterogeneity.

```    
conda env create -f requirements.txt
conda activate cnv_heterogeneity
```

# Running

`python get_group_clusters.py`

The script `get_group_clusters.py` takes the CNA profiles as input and output "group_clusters" that samples with CNV profile distance lower than a threshold would be assigned to the same "group cluater".

`python group_clusters_analysis.py`

The script `group_clusters_analysis.py` takes the "group clusters" that we get in the previous step and apply a second clustering on the CNV feature matrix, and finally output the "group cluster" with similar CNV pattern. 

By applying more analysis including analyse the distribution of the original NCIt entities we can systematically analyse the relationship between biological facts of CNV and NCIt cancer classification system.


# Visualization

The users can visualize the CNV profiles of specific biosamples on [progenetix](https://progenetix.org/) database by simply type in biosample ids.

![sample plot](https://github.com/ziyingyang96/cnv-heterogeneity/blob/main/pgxbs-kftvgk90.png)
