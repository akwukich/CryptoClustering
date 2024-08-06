# Module 11 Challenge
## CryptoClustering

## Background


The purpose of this challenge was to use the K-means algorithm and principal component analysis (PCA) to classify cryptocurrencies according to their price fluctuations over intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year.


## Installation


The following libraries and dependencies are required to successfully run the project:
- import pandas as pd
- from sklearn.cluster import KMeans
- from sklearn.decomposition import PCA
- from sklearn.preprocessing import StandardScaler


## Repository Files and Starter Code
- Resources folder: contains crypto_market_data.csv DataFrame provided in the starter code materials

- Crypto_Clustering.ipynb: completed notebook with data analysis, visualizations, and solutions/answers

## Methodology
The project was completed in seven steps:
1. Prepare the Data
2. Find the best value for k using original scaled DataFrame
3. Cluster cyptocurriencies with K-means using the original scaled DataFrame
4. Optimize Clusters with Principal Component Analysis to reduce the number of factors in the dataset and determie  which features have the strongest influence on the PCA components.
    - Find the best value for k using PCA Data
    - Cluster cyptocurriencies with K-means using the PCA Data
    - Determine the Weights of Each Feature on Each Principal Component

## Solutions/Answers

- **Question:** What is the best value for k?
  
        Based on purely visual inspection of the graph, the "elbow point" is at k=4 because it is the first point on the line graph where the decrease in inertia is less steep and, therefore, slows down. I also confirmed this by calculating the rate of decrease between each k-value, which demonstrated the percentage decrease slowed between k=4 and k=5.


**Question:** What is the total explained variance of the three principal components?
        The three principal components account for 37.2%, 34.7%, and 17.6% or 89.5% of the total variance. Put another way, about 90% of the total variance is condensed into the 3 PCA variables.

- **Question:**: What is the best value for k when using the PCA data?
        Based on purely visual inspection of the graph, the "elbow point" is at k=4 because it is the first point on the line graph where the decrease in inertia is less steep and, therefore, slows down. I also confirmed this by calculating the rate of decrease between each k-value, which demonstrated the percentage decrease slowed between k=4 and k=5.

- **Question:** Does it differ from the best k value found using the original data?
        No.
        

- **Question:** Question: Which features have the strongest positive or negative influence on each component?
        PCA1: price_change_percentage_200d and price_change_percentage_1y both have moderately strong positive correlations with PCA1 because their component weights were 0.59 and 0.57, respectively.

        PCA2: price_change_percentage_30d and price_change_percentage_14d both have moderately strong positive correlations with PCA1 because their component weights were 0.56 and 0.54, respectively.

        PCA3: price_change_percentage_7d strong positive correlation b/c component weight was 0.79


## Resources Consulted
For this challenge, I consulted the [Module 11 Starter Code](https://static.bc-edx.com/ai/ail-v-1-0/m11/lms/starter/M11_Starter_Code.zip)
 








