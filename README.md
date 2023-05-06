# CryptoClustering
The requirements for this challenge were to use unsupervised learning technique of k-Means clustering to group cryptocurrencies by their performance to create portfolio portfolio recommendations.

### Data Used
[crypto_market_data.csv](/Resources/crypto_market_data.csv) - market data of different cryptocurrencies during different time periods

### Summary
Using the elbow curve method to normalize the data to find the optimal k value for the k-Means model that will use all of the original features of the dataset. 

![Elbow curve plot showing a value of 4 for k to be optimal for the dataset with all features](/Resources/kvalues_elbow_curve.png) 

A k-Means model was trained and predicted using the best k values, resulting in four clusters of cryptocurrencies. The inertia of each cluster was large enough to consider reducing the number of features.

![A scatter plot showing 4 clusters with heavy inertia](/Resources/scatter_plot_crypto_currency.png)

To reduce the amount of features used, the Principal Component Analysis (PCA) was applied to create three primary clusters.

![DataFrame holding 3 primary clusters as columns and cryptocurrency as index](/Resources/PCA_analysis.png)

Then the PCA data was used to recalculate the optimal k value for the k-Means model.

![Elbow curve line plot from the PCA data that shows 4 to be the optimal k value](/Resources/pca_k_values_elbow_curve.png)

Finally, a new cluster was drawn using the best k value of the PCA feature.

![Scatter plot showing 4 low inertia clusters generated using the PCA dataframe](/Resources/scatter_plot_crypto_currency.png)