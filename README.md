# CryptoClustering

## Task

## Instructions

1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

2. Load the crypto_market_data.csv into a DataFrame.

3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

## Prepare the Data

se the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the Original Scaled DataFrame

Use the elbow method to find the best value for k using the following steps:

Create a list with the number of k values from 1 to 11.

Create an empty list to store the inertia values.

Create a for loop to compute the inertia with each possible value of k.

Create a dictionary with the data to plot the elbow curve.

Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following question in your notebook: What is the best value for k?

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data

Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

Initialize the K-means model with the best value for k.

Fit the K-means model using the original scaled DataFrame.

Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.

Create a copy of the original data and add a new column with the predicted clusters.

Create a scatter plot using hvPlot as follows:

Set the x-axis as "PC1" and the y-axis as "PC2".

Color the graph points with the labels found using K-means.

Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Optimize Clusters with Principal Component Analysis

Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

What is the total explained variance of the three principal components?

Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the PCA Data

Use the elbow method on the PCA data to find the best value for k using the following steps:

Create a list with the number of k-values from 1 to 11.

Create an empty list to store the inertia values.

Create a for loop to compute the inertia with each possible value of k.

Create a dictionary with the data to plot the Elbow curve.

Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

Answer the following question in your notebook:

What is the best value for k when using the PCA data?

Does it differ from the best k value found using the original data?


## Cluster Cryptocurrencies with K-means Using the PCA Data

Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

Initialize the K-means model with the best value for k.

Fit the K-means model using the PCA data.

Predict the clusters to group the cryptocurrencies using the PCA data.

Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

Create a scatter plot using hvPlot as follows:

Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".

Color the graph points with the labels found using K-means.

Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

Answer the following question:

What is the impact of using fewer features to cluster the data using K-Means?

## Description

I started by renaming the notebook provided to 'crypto_clustering.iypnb. I imported the required libraries and dependencies. I loaded the CSV into a pandas DataFrame indexing the columns to the 'coin-id'. Described the data and plotted the data in a line plot with the code provided. I started preparing the data using the 'StandardScaler()' module to normalize the data. Created a DataFrame with the scaled data. Copied the crypto names and indexed them to the newly created DataFrame. To find the best value for k using the original data, I started by creating a list with the number of k-values from 1 to 11. Created an empty list to store the inertia values. Created a KMeans model using the loop counter for the n_clusters. Fit the model to the data, Appended the model.inertia_ to the inertia list. I then created a dictionary with the data to plot the elbow curve, Created and sampled this data as a DataFrame, and plotted the elbow curve to determinethe best k value which was 4. To cluster the cryptocurrencies with K-Means using the original data, I initialized the K_Means model using the k value of 4. I fit the model using the scaled data. Predicted the clusters to group the cryptocurrencies using the scaled data. Created a copy of the scaled data DataFrame and added a new column for the predicted clusters. Created a scatter plot visualizing the clusters with the parameters provided. To optimize the clusters with Principal Component Analysis, I created the PCA model instance. Used the PCA model with fit.transform to reduce to three principal components, retrieved the explained variance, and determined the total explained variance of the three principal components being approximately 89%. Created a DataFrame with the PCA data To find the best value for k using the PCA data, I used the same methodology used with the original data. I then optimized the cluster cryptocurrencies with K-means using the PCA data with the same methodology used with the original data. I then created composites for both elbow curve and scatter plots for the original and pca data. After visualizing, the PCA data points seem more compactly clustered, therefore showing the impact that using fewer features, makes for easier interpretation.
