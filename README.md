# CryptoClustering
The requirements for this challenge were to use unsupervised learning technique of k-Means clustering to group cryptocurrencies by their performance to create portfolio portfolio recommendations.

### Data Used
[crypto_market_data.csv](/Resources/crypto_market_data.csv) - market data of different cryptocurrencies during different time periods

### Summary
Using the elbow curve method to normalize the data to find the optimal k value for the k-Means model that will use all of the original features of the dataset. 

![pca k values elbow curve](https://user-images.githubusercontent.com/117309455/236635583-a91aea55-5341-47e8-a031-e79e3374b64a.png)

Elbow curve plot showing a value of 4 for k to be optimal for the dataset with all features

A k-Means model was trained and predicted using the best k values, resulting in four clusters of cryptocurrencies. The inertia of each cluster was large enough to consider reducing the number of features.

![scatter plot crypto currency](https://user-images.githubusercontent.com/117309455/236635620-f733ecd1-b258-488a-9790-4a956d28e364.png)

A scatter plot showing 4 clusters with heavy inertia

To reduce the amount of features used, the Principal Component Analysis (PCA) was applied to create three primary clusters.

![kvalues elbow curve](https://user-images.githubusercontent.com/117309455/236635634-f059c82d-598a-4b93-b8bf-d24c3da40f95.png)

DataFrame holding 3 primary clusters as columns and cryptocurrency as inde

Then the PCA data was used to recalculate the optimal k value for the k-Means model.

![image](https://user-images.githubusercontent.com/117309455/236635550-05fd515f-0703-4f8d-b99b-266b207bd53d.png)


Elbow curve line plot from the PCA data that shows 4 to be the optimal k value


Finally, a new cluster was drawn using the best k value of the PCA feature.

![primary clusters](https://user-images.githubusercontent.com/117309455/236635815-65a69092-e35a-4300-a406-dbf004247d1a.png)

Scatter plot showing 4 low inertia clusters generated using the PCA dataframe

---

## Technologies

This project uses Jupyter Notebook using a Python 3 kernel. 

Dependencies used: 
1. [Jupyter] - Running code 
2. [Conda] - Dev environment
3. [Pandas] - Data analysis
4. [Matplotlib] - Data visualization
5. [Numpy] - Data calculations & Pandas support
6. [hvPlot] - Interactive Pandas plots 
7. [scikit-learn] - kMeans clustering, PCA, and StandardScaler 

---
