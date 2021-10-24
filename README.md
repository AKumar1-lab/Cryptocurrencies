## Cryptocurrencies

Module 18 Cryptocurrencies and Unsupervised Machine Learning

Completed by Angela Kumar

## Purpose

Use unsupervised machine learning techniques to analyze cryptocurrency data.

## Overview

The machine learning techniques using unsupervised algorithms help us explore data when we're not sure what we're looking for. Now you can analyze data without a clear output in mind.

You'll work primarily with the K-means algorithm, the main unsupervised algorithm that groups similar data into clusters. We'll build on this by speeding up the process using principal component analysis (PCA), which employs many different features or variables.

## Resources

Data:  crypto_clustering_starter_code.ipynb converted to crypto_clustering.ipynb; crypto.csv

Technologies: Juypter Notebooks; Python mlenv; Pandas; plotly_express; hvplot;sklearn libraries for StandardScaler, MaxMinScaler; KMeans; PCA

## Background

You and Martha have done your research. You understand what unsupervised learning is used for, how to process data, how to cluster, how to reduce your dimensions, and how to reduce the principal components using PCA. It’s time to put all these skills to use by creating an analysis for your clients who are preparing to get into the cryptocurrency market.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

## Deliverables

##### Deliverable 1: Preprocessing the Data for PCA

Using your knowledge of Pandas, you’ll preprocess the dataset in order to perform PCA in Deliverable 2.

* The following five preprocessing steps have been performed on the crypto_df DataFrame:
* All cryptocurrencies that are not being traded are removed 
* The IsTrading column is dropped 
* All the rows that have at least one null value are removed 
* All the rows that do not have coins being mined are removed 
* The CoinName column is dropped 
* A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 
* The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X 
* The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function

###### Original DataFrame

<img width="481" alt="Orginal crypto DataFrame" src="https://user-images.githubusercontent.com/85860367/138583394-66a9a6b2-8af4-4b9e-8146-9c96d9151604.PNG">

###### DataFrame with Cryptocurrency Coin Names

<img width="513" alt="CoinName" src="https://user-images.githubusercontent.com/85860367/138583226-2bd51a84-8f7c-4cfe-8ed0-cfe55ae63642.PNG">

###### Crypto DataFrame

<img width="470" alt="Deliverable 1 screenshot" src="https://user-images.githubusercontent.com/85860367/138583058-5ff696d7-7d46-4e5a-a29a-7a68c966483b.PNG">


##### Deliverable 2: Reducing Data Dimensions Using PCA

Using your knowledge of how to apply the Principal Component Analysis (PCA) algorithm, you’ll reduce the dimensions of the X DataFrame to three principal components and place these dimensions in a new DataFrame.

* The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components (10 pt)
* The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame

###### PCS DataFrame

<img width="635" alt="Deliverable 2 screenshot" src="https://user-images.githubusercontent.com/85860367/138583070-ce0aa817-fa19-48c6-b94a-0ac06226939c.PNG">


##### Deliverable 3: Clustering Cryptocurrencies Using K-means

Using your knowledge of the K-means algorithm, you’ll create an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created in Deliverable 2. Then, you’ll run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

* The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
* An elbow curve is created using hvPlot to find the best value for K 
* Predictions are made on the K clusters of the cryptocurrencies’ data 
* A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 

###### Elbow Curve based on K-Means algorithms

<img width="557" alt="Elbow Curve Screenshot" src="https://user-images.githubusercontent.com/85860367/138583249-3fae793d-3cbd-4ee0-a672-2b7dba3bcf58.PNG">

###### Clustered DataFrame

<img width="661" alt="Clustered DataFrame" src="https://user-images.githubusercontent.com/85860367/138583684-9e33f1c6-1f49-48a9-a2ab-9ba3f0fe0024.PNG">


##### Deliverable 4: Visualizing Cryptocurrencies Results

Using your knowledge of creating scatter plots with Plotly Express and hvplot, you’ll visualize the distinct groups that correspond to the three principal components you created in Deliverable 2, then you’ll create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

* The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover 
* A table with tradable cryptocurrencies is created using the hvplot.table() function 
* The total number of tradable cryptocurrencies is printed 
* A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns 
* A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point 

###### 3D Plot

<img width="528" alt="3D Plot screenshot" src="https://user-images.githubusercontent.com/85860367/138583261-d085fff8-d7a6-48e8-9a45-124a390816b8.PNG">

###### Tradable Table

<img width="684" alt="Tradable Table screeshot" src="https://user-images.githubusercontent.com/85860367/138583274-cd80d96a-5187-4881-b8d8-0be09533d516.PNG">

###### Plot DataFrame

<img width="468" alt="New Plot DataFrame Screenshot" src="https://user-images.githubusercontent.com/85860367/138583282-63e5c659-8a5b-4e54-ae5b-d8bd356aa74d.PNG">

###### Scatter Plot using hvplot

<img width="575" alt="ScatterPlot screenshot" src="https://user-images.githubusercontent.com/85860367/138583292-90d6f2ac-d3c9-4da6-b214-471ca11a1f06.PNG">


### Summary

Overall, this project was very interesting, it helped to understand unsupervised vs. supervised machine learning.  Unsupervised Machine Learning algorithms try to analyze and search for anomolies, trends, patterns on unstructured datasets and/or without guidance.  There are no specific guidelines per se prescribed for the machine or the analyst  to make any analyses, and there are unwritten rules.   Unsupervised Machine Learning algorithms makes predictions, trends, and looks for pattern recognition or anomolies using K-Means, hieracrchial clustering,  Pricipal Component Analysis(PCA) and Natural Language Processing.  Another key aspect is the reduction of the data to more useful size.  The dataset also is reduced to a smaller sample size to work with to uncover the trends, patterns and anomolies.  Unsupervised Machine Learning algorithms are extremely useful in emerging industries such as biotechnology, health, biology, finance, cybersecurity, pricing, customer preferences. 




