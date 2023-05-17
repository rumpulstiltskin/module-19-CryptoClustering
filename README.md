# CryptoClustering

Repository for Module 19 Challenge

## Technologies

This project leverages python 3.7 with the following packages:

* [pandas](https://pandas.pydata.org/docs/) - For the analysis of dataframes.

* [sklearn](https://scikit-learn.org/stable/) - For the creation of the clusters.

* [hvplot](https://hvplot.holoviz.org/user_guide/Introduction.html) - For the creation of the interactive visualizations.

* [plotly](https://plotly.com/python/) - For the creation of the interactive visualizations.

## Data

The data used for this project was provided by the Data Analytics Bootcamp, and it is in the [Resources](Resources/crypto_market_data.csv) folder of this repository.

---

## Project Description

In this challenge, we will use unsupervised learning to analyze data on the cryptocurrencies traded on the market. We will group the cryptocurrencies together to create a classification system for clusters. To do so, we will use a clustering algorithm to help determine performance similarities and differences of cryptocurrencies. Then, we will create plots, and data tables to present our results.

We will use the following steps for this challenge:

1. Prepare the data for clustering using K-means.

2. Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.

3. Reduce data dimensions using PCA algorithms from sklearn.

4. Predict clusters using cryptocurrencies data using the PCA algorithm and K-means.

5. Create some plots and data tables to present the results.

---

## Observations and Insights

The data contains 41 cryptocurrencies with 7 features which are price change percentage over various timeframes. The clustering was done with 2 methods, one without PCA and one with PCA. The resulting plots show the differences when only scaling the original data and when scaling the data after applying PCA. The plot using the original data is using the first 2 features: one day and one week. Though the model was trained on all the data the plot only shows the first 2 features and with the currencies being so volatile over the course of the year, the plot is not as useful. The plot using PCA shows the first 2 principal components and the clusters are much more defined. This makes the plot much more useful for investors to see which currencies are similar and which are different. Both plots show that there are 2 outlier currencies which occupy their own groups, but the original data plot has one positioned amongst another group. This is because the visualization itself is displaying an incomplete version of the data as it's plotted on the first 2 features.

The elbow curve shows that the optimal number of clusters is 4. This is because the curve is showing the inertia of the model as the number of clusters increases. The inertia is the sum of squared distances from each point to its assigned centroid. The inertia decreases as the number of clusters increases. The elbow curve shows that the inertia decreases significantly from 1 to 4 clusters, but then the decrease is much less significant from 4 to 5 clusters. This is why 4 is the optimal number of clusters.
