<!-- # Introduction
This repository provides the code for the manuscript titled "Peeking Through the Homelessness System with a Network Science Lens" by Charalampos Chelmis and Khandker Sadia Rahman.

## Citation
To cite our paper, please use the following reference:

Charalampos Chelmis and Khandker Sadia Rahman "Peeking Through the Homelessness System with a Network Science Lens." IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining (ASONAM '21). doi: 10.1145/3487351.3488321.

BibTeX:
``` 
@article{chelmis2021asonam, 
  author = {Chelmis, Charalampos and Rahman, Khandker Sadia},
  title = {Peeking through the Homelessness System with a Network Science Lens},
  year = {2021},
  isbn = {9781450391283},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3487351.3488321},
  doi = {10.1145/3487351.3488321},
  booktitle = {Proceedings of the 2021 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining},
  pages = {69–73},
  numpages = {5},
  keywords = {socially important data science, computational social science, applied network science, human services},
  location = {Virtual Event, Netherlands},
  series = {ASONAM '21}
}
```


## Quick Overview
We computationally analyze a one of a kind individual-level longitudinal homelessness dataset to further our understanding of how individuals progress through the homelessness system with the ultimate goal of securing stable housing. We model the homelessness system as a network of interconnected services which individuals traverse over time and we formalize the concept of stability upon exit of the system. We show that regardless of starting conditions, the ultimate goal is either reached quickly or not at all, indicating the importance of addressing the homeless’ needs early on to avoid them "giving up". Next, we formalize similarity between homeless services inspired by a view of the homelessness system as a heterogeneous network. We show that in its current form the homelessness system is inefficient in promoting trajectories towards positive outcomes.-->


### Prerequisites
Python 2.7 or above and the following libraries
```
pandas, mumpy, matplotlib, os, sklearn,
```

### Files
```
   ToyDataset.csv: A sample dataset with the features and trajectories. 
   step1_Complete Trajectory Adjacency list preparation for Project ID.ipynb: Creates an adjacency list for the network of project ids 
   step1_Complete Trajectory Adjacency list preparation for Project Type.ipynb: Creates an adjacency list for the network of project types
   step2_One hot encoding.ipynb: Prepares the one hot encoded version of the dataset.
   step3_Scheme 1 analysis.ipynb: Prepares and analyses the dataset for scheme 1. 
   step3_Scheme 2 analysis.ipynb: Prepares and analyses the dataset for scheme 2. 
   step3_Scheme 3 analysis.ipynb: Prepares and analyses the dataset for scheme 3. 
   step4_Link probability of project ID for figure 5.ipynb: Calculates the link probability for the network of project ids.
   step4_Link probability of project type for figure 5.ipynb: Calculates the link probability for the network of project types.
   step4_Link probability of project ID versus project type.ipynb: Compares the link probability of both the networks.
   step5_TF_IDF to the next.ipynb: Analyses the similarity between the current and the next project type
   step5_TF_IDF to the target.ipynb: Analyses the similarity between the current and target project type.
   step_6_Cosine similarity computation at each step for project type.ipynb: Computes the cosine similarity between project types for each step.
   step_6_Cosine similarity trends to the actual exit.ipynb: Computes the cosine similarity of project type at each step to the actual exit.
   step_6_Cosine similarity trends to the next project type.ipynb: Computes the cosine similarity of current project type at each step to the next project type.
   step_6_Cosine similarity trends to ultimate goal.ipynb: Computes the cosine similarity of project type at each step to ultimate goal.
   step_7_Similarity between living situation and the ultimate goal.ipynb: Computes the similarity between initial living situation with the ultimate goal.
   step_7_Similarity of first and last step project type with the ultimate goal.ipynb: Computes the similarity between first step (and last step) with the ultimate goal.
   step_8_Why give up? outdegree,indegree.ipynb: Comptues the outdegree and indegree.
   step_8_Why give up? page rank.ipynb: Computes the page rank.
   step_9_Cycle_average no of backlink per mission .ipynb: Computes the average number of backlink per mission.
   step_9_Cycle_percent atleast one backlink.ipynb: Computes the percent of at least one backlink.
   step_10_Why paths go backward?.ipynb: Computes probability of backlinks conditioned on change (and no change) in cosine similarity at the previous step.   
   
```

### How to use
The toy dataset shows a snippet of the data used after data cleaning and feature preprocessing have been done. This data can be directly run through the jupyter notebook files for the following purposes:

1. Prepare the adjacency lists for the two transistion graphs: (i) network of project ids and (ii) network of project types.
2. Create a separate set of data, labelling each entry and exit point as per the scheme under observation. 
3. Analyse the reentry, success, and dropout porbabilities for the different schemes.
4. Plot the cumulative distribution function for each scheme. 
5. Prepare and analyse the link probability for both the networks of project types and ids.
6. Anaylse the similarity between project types and their similarity with the target. 
7. Analyse the similarity of initial living situation and project type at first step (and last step) with ultimate goal
8. Analyse the outdegree, indegree, and page rank.
9. Analyse cycle in trajectories and appearance of backlinks with changes in cosine similarity at the prviouse step
