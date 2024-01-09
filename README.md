# Country Segmentation Unsupervised Machine Learning

## Introduction
This task involves the application of machine learning clustering algorithms, specifically the k-means and Mean-Shift model, to a country dataset containing economic and social indicators. Unsupervised machine learning is utilised to unveil hidden patterns within the data, with clustering being a prevalent technique for identifying groupings in a dataset with features and observations.
## K-means:
K-means, a centroid-based clustering algorithm, involves setting a predetermined number of clusters (k) and assigning each data point in the dataset to these clusters based on Euclidean distance. The algorithm iteratively recalculates the centroids' positions by computing the mean of all data points assigned to each cluster until an optimal fit is achieved. 
## Mean-Shift:
In contrast, does not require a predefined number of clusters. Instead, it assigns each data point to the peaks it identifies in the dataset, focusing on locating high-density areas. This makes Mean-Shift particularly valuable when the number of clusters is unknown.

## Model Construction and Implementation
Data undergoes pre-processing and exploratory analysis to ensure suitability. Key features, such as exports (range 0 to 200) and imports (range 0 to 174), exhibit a high positive correlation. Child mortality ranges from 2 to 208. A simple k-means and meanshift algorithm is deployed, clustering based on child mortality and exports before progressing to more inclusion of the other features. 

## Observations
The K-means model efficiently grouped the dataset into five clusters. Notably, Cluster 3 represents countries with low child mortality and limited exports, reflecting good healthcare and socio-economic conditions. Cluster 0 is the most favorable, with low child mortality and high exports. Cluster 2 has better child mortality rates and substantial exports. Cluster 4 shows higher child mortality and poor exports, while Cluster 1 includes countries with poor performance in both child mortality and exports, with some outliers having average export performance.

## Comparison of Mean-Shift and k-Means
Mean-Shift and k-Means clustering methods yield distinct outcomes. k-Means suggests around 5 optimal clusters, while Mean-Shift favors a more effective 3-cluster approach. Across various input variables, k-Means (5 clusters) provides richer insights, with similarities noted in k-Means cluster 0 and Mean-Shift cluster 1. Discrepancies arise in features like import and exports, where k-Means suggests 3 clusters, and Mean-Shift reports 4. Further exploration with three features reveals differences in optimal clusters (6 for k-Means and 3 for Mean-Shift) and unique cluster assignments for specific data points.

# Evaluation and Recommendations
The K-means elbow plot technique, initially used to determine the optimal number of clusters, was further assessed using silhouette score for accuracy verification. More features from the dataset were incorporated, and both K-means and mean-shift models were applied to gain further insights, proving to be beneficial. Throughout the algorithmic procedure, both models consistently identified a cluster with 3 or 4 data points, signifying the best-performing countries based on economic and social indicators. Further Python analysis, by assigning these clusters to the full dataset, revealed these countries to be **Luxembourg**, **Switzerland**, **Qatar**, and **Singapore**. Occasionally, a fifth country, **Norway**, was also identified


