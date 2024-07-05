# CryptoClustering

## Introduction

This project uses Python and unsupervised learning techniques to analyze if cryptocurrencies are affected by 24-hour or 7-day price changes. The main goal is to perform clustering using K-Means and Principal Component Analysis (PCA) on cryptocurrency market data.

## Repository Setup

1. Create a new repository named `CryptoClustering`.
2. Clone the repository to your local machine.

## Steps

### 1. Data Preparation

- Load `crypto_market_data.csv` into a DataFrame.
- Normalize the data using `StandardScaler` from scikit-learn.
- Create a DataFrame with the scaled data and set the "coin_id" index.

### 2. Determine the Best Value for k

- Use the elbow method on both the original scaled data and the PCA-transformed data to find the optimal value for k.
- Plot the elbow curve to visualize the optimal k value.

### 3. Clustering with K-Means

- **Original Data:** 
  - Initialize and fit the K-means model.
  - Predict clusters and visualize using a scatter plot with hvPlot.
- **PCA Data:** 
  - Perform PCA to reduce features to three principal components.
  - Initialize and fit the K-means model using PCA data.
  - Predict clusters and visualize using a scatter plot with hvPlot.

### 4. Analysis and Comparison

- Create composite plots to compare the results from the original data and the PCA data.
- Analyze the impact of using fewer features for clustering.

### What is the best value for k?

**Answer:** The best value based on the Elbow curve is 4.

### What is the total explained variance of the three principal components?

**Answer:** The total variance of the three components is about 89.5%, which means that 89.5% of all the data's variance is captured by these three PCA variables.

### What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

**Answer:** 
- The best value for k is 4, based on the elbow curve graph.
- No, it does not differ from the original data.

### What is the impact of using fewer features to cluster the data using K-Means?

**Answer:** The PCA-transformed data, which uses fewer features, provides a clearer separation of the clusters. In this case, it separates the clusters better, making the distinctions between different groups more evident.



