

# Clustering Analysis with K-Means and PCA for Cryptocurrency Data

## Project Overview

This project explores clustering different cryptocurrencies using K-Means. We perform clustering twice:
1. Using the original cryptocurrency data.
2. After applying **Principal Component Analysis (PCA)** to reduce the number of features.

The goal is to compare how using fewer features impacts the clustering of the coins.

## Goals

1. Perform K-Means clustering on the original cryptocurrency data.
2. Use PCA to reduce the data to key components.
3. Find the elbow curve for both the original and PCA data to determine the optimal number of clusters.
4. Compare the clustering results from the original data and PCA-transformed data.

## Steps


1. **Data Preprocessing**: 
   - Load and scale the cryptocurrency data.

2. **Elbow Method for Original Data**: 
   - Generate an elbow curve to identify the optimal number of clusters for the original dataset.

3. **K-Means on Original Data**: 
   - Perform K-Means clustering based on price changes over 24 hours and 7 days, using the optimal K-value identified from the elbow method.

4. **PCA Transformation**: 
   - Reduce the dataset to three principal components (PC1, PC2, PC3) and calculate the total explained variance, which is approximately **85.50%**.

5. **Elbow Method for PCA Data**: 
   - Generate an elbow curve to find the optimal number of clusters for the PCA-transformed dataset.

6. **K-Means on PCA Data**: 
   - Perform K-Means clustering on the reduced data using the optimal K-value from the PCA elbow method.

7. **Comparison**: 
   - Visualize the clusters from both the original and PCA-transformed data side by side.

## Results

![Elbow Curve Comparison](https://github.com/mariemsdiaz/CryptoClustering/blob/main/Unsupervised_Machine_Learning/Resources/Elbow_Curve.png)
![PCA Scatter Plot Comparison](https://github.com/mariemsdiaz/CryptoClustering/blob/main/Unsupervised_Machine_Learning/Resources/Cluster_Plot.png)


## Conclusion
Using PCA for clustering, we can observe that some cryptocurrencies, which were previously close to other clusters, are now identified as outliers in the graph. For instance, Cluster 1 (coin_id = "celsius-degree-token") was grouped with other coins in the original scatter plot, but it is now more isolated. Similarly, the token EthLend in Cluster 3 is also identified as an outlier, although it has moved slightly closer to other points compared to the original data.

This analysis demonstrates that we can effectively highlight the story of these outliers while working with a simpler dataset. In conclusion, PCA reduces the complexity of the data, which can enhance the efficiency of clustering. However, there may be a trade-off between simplification and the potential loss of detail from the original dataset. The elbow curves for both the original and PCA-transformed datasets serve as valuable tools in selecting the optimal number of clusters for analysis.

### End Note 

This analysis was completed and performed with the help of past class activities on machine learning, the use of ChatGPT for rapidly answer questions and generate code solutions. 