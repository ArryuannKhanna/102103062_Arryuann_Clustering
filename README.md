# Clustering Analysis on Heart Failure Clinical Records

This project is a comprehensive study on clustering analysis applied to the Heart Failure Clinical Records dataset from the UCI Machine Learning Repository. Using the PyCaret library, we explore various clustering algorithms to uncover inherent groupings within the data.

## Dataset

The dataset for this analysis is the Heart Failure Clinical Records dataset, which can be accessed [here](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records). It consists of multiple features related to heart disease conditions in patients, which are used to predict mortality by heart failure.

## PyCaret: An Automated Machine Learning Library

[PyCaret](https://pycaret.org/) is an open-source, low-code machine learning library in Python that automates machine learning workflows. It is an end-to-end machine learning and model management tool that speeds up the experiment cycle exponentially.

## Clustering Algorithms

In this study, we employ several clustering algorithms to evaluate their performance on the dataset:

### K-Means Clustering

K-Means clustering is a method of vector quantization that aims to partition 'n' observations into 'k' clusters in which each observation belongs to the cluster with the nearest mean.

![K-Means Clustering Graph](path_to_kmeans_graph)

### Hierarchical/Agglomerative Clustering

Agglomerative clustering is a type of hierarchical clustering that builds nested clusters by merging or splitting them successively. This hierarchy of clusters is represented as a tree (or dendrogram).

![Hierarchical Clustering Graph](path_to_hierarchical_graph)

### Mean Shift Clustering

Mean shift clustering is a sliding-window-based algorithm that assigns the data points to the clusters iteratively by shifting points towards the mode (the highest density of data points in the region).

![Mean Shift Clustering Graph](path_to_meanshift_graph)

### Affinity Propagation

Affinity propagation creates clusters by sending messages between pairs of samples until convergence. Unlike K-Means, it does not require the number of clusters to be determined or estimated before running the algorithm.

![Affinity Propagation Graph](path_to_affinity_graph)

### Spectral Clustering

Spectral clustering uses the spectrum (eigenvalues) of the similarity matrix of the data to perform dimensionality reduction before clustering in fewer dimensions.

![Spectral Clustering Graph](path_to_spectral_graph)

## Comparative Study

We compare the performance of the above algorithms using various pre-processing techniques and different numbers of clusters. The evaluation is based on parameters such as the Silhouette Score, Calinski-Harabasz Index, and Davies-Bouldin Index.

### Sample Result Table

## Performance using different clustering techniques on various parameters

### Using K-Mean Clustering

| Parameters        | No Data Processing | | | Using Normalization | | | Using Transform | | | Using PCA | | | Using T+N | | | T+N+PCA | | |
|-------------------|--------------------|----|----|---------------------|----|----|-----------------|----|----|-----------|----|----|---------|----|----|---------|----|----|
|                   | c=3                | c=4 | c=5 | c=3                 | c=4 | c=5 | c=3             | c=4 | c=5 | c=3      | c=4 | c=5 | c=3    | c=4 | c=5 | c=3    | c=4 | c=5 |
|-------------------|--------------------|----|----|---------------------|----|----|-----------------|----|----|-----------|----|----|---------|----|----|---------|----|----|
| Silhouette        | 0.74               | 0.72 | 0.68 | 0.69                | 0.61 | 0.55 | NA              | NA  | NA  | 1         | 1    | 1    | 0.54    | 0.43 | 0.35 | 0.54    | 0.44 | 0.36 |
| Calinski-Harabasz | 3567               | 5012 | 4683 | 6633                | 7654 | 7999 | NA              | NA  | NA  | 5294      | 7207 | 1110 | 1109    | 1245 | 1152 | 1190    | 1290 | 1202 |
| Davies-Bouldins   | 0.34               | 0.41 | 0.46 | 0.59                | 0.67 | 0.77 | NA              | NA  | NA  | 0.39      | 0.41 | 0.63 | 0.63    | 0.77 | 0.95 | 0.62    | 0.75 | 0.92 |


### Using Hierarchical Clustering

| Parameters       | No Data Processing | Using Normalization | Using Transform | Using PCA | Using T+N | T+N+PCA |
|------------------|--------------------|---------------------|-----------------|-----------|-----------|---------|
| Silhouette (c=3) | 1                  | 0.53                | NA              | 1         | 0.56      | 0.48    |
| Silhouette (c=4) | 1                  | 0.49                | NA              | 1         | 0.47      | 0.48    |
| Silhouette (c=5) | 1                  | 0.53                | NA              | 1         | 0.48      | 0.48    |
| Calinski-Harabasz| 2766               | 1107                | NA              | 2766      | 3797      | 3598    |
| Calinski-Harabasz| 2766               | 1693                | NA              | 1107      | 3598      | 3329    |
| Calinski-Harabasz| 2766               | 2028                | NA              | 1107      | 3598      | 3867    |
| Davies-Bouldins  | 0.99               | 0.14                | NA              | 0.09      | 0.57      | 0.71    |
| Davies-Bouldins  | 0.14               | 0.18                | NA              | 0.14      | 0.72      | 0.77    |
| Davies-Bouldins  | 0.18               | 0.60                | NA              | 0.71      | 0.78      | 0.77    |

### Using K-mean Shift Clustering

| Parameters       | No Data Processing | Using Normalization | Using Transform | Using PCA | Using T+N | T+N+PCA |
|------------------|--------------------|---------------------|-----------------|-----------|-----------|---------|
| Silhouette (c=3) | 0.99               | 0.53                | NA              | 1         | 0.56      | 0.48    |
| Silhouette (c=4) | 0.99               | 0.50                | NA              | 1         | 0.47      | 0.48    |
| Silhouette (c=5) | 0.99               | 0.53                | NA              | 1         | 0.48


> **Note**: The table will be filled in with actual results from the analysis.

## Conclusion

The results of this study provide valuable insights into the characteristics of different clustering algorithms when applied to medical data. The effectiveness of each algorithm varies based on the pre-processing techniques and the intrinsic structure of the data.

---
Generated by [PyCaret](https://pycaret.org/) and analyzed by [Author/Team Name].
