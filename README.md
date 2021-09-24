# Introduction
This repository provides the full code and results for the manuscript titled "Peeking Through the Homelessness System with a Network Science Lens" by Charalampos Chelmis and Khandker Sadia Rahman.

## Quick Overview
We computationally analyze a one of a kind individual-level longitudinal homelessness dataset to further our understanding of how individuals progress through the homelessness system with the ultimate goal of securing stable housing. We model the homelessness system as a network of interconnected services which individuals traverse over time and we formalize the concept of stability upon exit of the system. We show that regardless of starting conditions, the ultimate goal is either reached quickly or not at all, indicating the importance of addressing the homeless’ needs early on to avoid them "giving up". Next, we formalize similarity between homeless services inspired by a view of the homelessness system as a heterogeneous network. We show that in its current form the homelessness system is inefficient in promoting trajectories towards positive outcomes.


### Prerequisites
Python 2.7 or above and the following libraries
```
pandas, mumpy, matplotlib, os, sklearn
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
```

### How to use
The toy dataset shows a snippet of the data used after data cleaning and feature preprocessing have been done. This data can be directly run through the jupyter notebook files for the following purposes:

1. Prepare the adjacency lists for the two transistion graphs: (i) network of project ids and (ii) network of project types.
2. Create a separate set of data, labelling each entry and exit point as per the scheme under observation. 
3. Analyse the reentry, success, and dropout porbabilities for the different schemes.
4. Plot the cumulative distribution function for each scheme. 
5. Prepare and analyse the link probability for both the networks of project types and ids.
6. Anaylse the similarity between project types and their similarity with the target. 

You may look for inspiration on the structure and kind of text to include in existing repos. For instance, https://github.com/ogencoglu/fair_cyberbullying_detection

