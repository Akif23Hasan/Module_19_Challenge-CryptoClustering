# Module_19 - Crypto Clustering

## Overview
In this assignment, we will be working with cryptocurrency data to perform clustering using the K-means algorithm. The goal is to identify the best value for `k` (number of clusters) using both the original scaled data and PCA-transformed data, and then compare the results.

## Requriements
* Python v3.10.9
* Pandas: A library for data manipulation and analysis.
* Numpy: A library for numerical operations and array manipulation.
* Hvplot.pandas: A library for interactive plotting and visualization.
* Scikit-learn: A library for machine learning and data preprocessing, including K-means clustering and PCA.

## Resources
The crypto_market_data dataset is required for this assignment. It is saved in the resources folder of the GitHub repository associated with this project. This dataset contains the necessary cryptocurrency market data for clustering analysis.

Note: Please ensure that you have the required dataset in the specified location to successfully run the code and perform the clustering analysis.

## Dataset Preparation
To begin, we need to prepare the data by normalising it using the StandardScaler() module from scikit-learn. This will ensure that the data is scaled properly for clustering. We will create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Finding the Best Value for `k` using the Original Scaled DataFrame
Next, we will use the elbow method to find the best value for `k` for clustering using the original scaled DataFrame. The elbow method involves the following steps:

1. Create a list with the number of `k` values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Compute the inertia with each possible value of `k`.
4. Create a dictionary with the data to plot the elbow curve.
5. Plot a line chart with the inertia values to visually identify the optimal value for `k`.
6. Answer the question: What is the best value for `k`?

## Clustering Cryptocurrencies with K-means Using the Original Scaled Data
Once we have determined the best value for `k`, we will perform clustering on the original scaled data. The steps involved are:

1. Initialise the K-means model with the best value for `k`.
2. Fit the K-means model using the original scaled DataFrame.
3. Predict the clusters and group the cryptocurrencies.
4. Create a scatter plot to visualise the clusters using hvPlot.
5. Answer any relevant questions about the impact of clustering on the original scaled data.

## Optimising Clusters with Principal Component Analysis (PCA)
In order to further optimise the clustering, we will perform Principal Component Analysis (PCA) on the original scaled DataFrame. This will reduce the dimensionality of the data while retaining the most important information. We will retrieve the explained variance to determine the information attributed to each principal component and answer the question: What is the total explained variance of the three principal components?

## Finding the Best Value for `k` using the PCA Data
Next, we will use the elbow method on the PCA data to find the best value for `k`. This involves the same steps as before: creating a list of `k` values, computing the inertia, plotting the elbow curve, and determining the optimal value for `k`. We will also answer the question: Does it differ from the best `k` value found using the original data?

## Clustering Cryptocurrencies with K-means Using the PCA Data
Finally, we will cluster the cryptocurrencies using the best value for `k` obtained from the PCA data. The steps involved are similar to clustering with the original scaled data, but using the PCA-transformed DataFrame. We will create a scatter plot to visualise the clusters and answer any relevant questions about the impact of using fewer features for clustering.

## Conclusion
By completing this assignment, we will gain a deeper understanding of clustering techniques, the impact of data transformation using PCA, and the importance of finding the optimal number of clusters (`k`) for effective analysis.
