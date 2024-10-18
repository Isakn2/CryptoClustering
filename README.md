# Crypto Clustering

## Overview

This project demonstrates clustering analysis on cryptocurrency data using K-Means. It leverages machine learning techniques, such as Principal Component Analysis (PCA) for dimensionality reduction and K-Means clustering, to identify potential groups within the cryptocurrency market based on various price change metrics.

## Dataset

The dataset used in this project includes cryptocurrency market data with the following key features:
- **price_change_percentage_24h**: Percentage change in price over the last 24 hours.
- **price_change_percentage_7d**: Percentage change in price over the last 7 days.
- **price_change_percentage_14d**: Percentage change in price over the last 14 days.
- **price_change_percentage_30d**: Percentage change in price over the last 30 days.
- **price_change_percentage_60d**: Percentage change in price over the last 60 days.
- **price_change_percentage_200d**: Percentage change in price over the last 200 days.
- **price_change_percentage_1y**: Percentage change in price over the last year.

The data is sourced from a CSV file, `crypto_market_data.csv`, which is loaded into a Pandas DataFrame for analysis.

## Process

### 1. Data Preparation
The dataset is normalized using `StandardScaler` to scale the features, ensuring that clustering algorithms like K-Means can function effectively without bias from feature magnitudes.

### 2. Elbow Method to Find Optimal `k`
The project implements the elbow method on the original scaled data to determine the optimal number of clusters (k) for K-Means. This is done by plotting inertia against various values of `k`.

### 3. PCA for Dimensionality Reduction
Principal Component Analysis (PCA) is applied to reduce the dimensionality of the data while preserving the most critical variance. This simplifies the data and helps in visualizing the clusters in 2D.

### 4. K-Means Clustering
The K-Means algorithm is run on both the original scaled data and the PCA-transformed data to create clusters. These clusters are then visualized using scatter plots for comparison.

## Visualizations

- **Elbow Curves**: To determine the optimal number of clusters, elbow curves for both the original and PCA-transformed data are plotted.
- **Cluster Scatter Plots**: The clusters are visualized based on both the original features and the PCA-reduced features, providing insights into how well the data is grouped.

## Key Libraries Used
- `pandas`: For data manipulation and analysis.
- `hvplot`: For creating interactive plots.
- `scikit-learn`: For machine learning algorithms such as K-Means, PCA, and StandardScaler.

## How to Use

1. Load the dataset (`crypto_market_data.csv`).
2. Follow the data preparation steps to scale the features.
3. Use the elbow method to identify the best value of `k` for clustering.
4. Apply K-Means clustering on both the original and PCA-reduced data.
5. Visualize and compare the clustering results.

## Conclusion

This project provides a framework for clustering cryptocurrencies based on price movement data, demonstrating the impact of dimensionality reduction and the K-Means algorithm on market data.