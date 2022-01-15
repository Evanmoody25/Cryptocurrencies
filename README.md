# Cryptocurrencies

# Overview of Project
You and Martha have done your research. You understand what unsupervised learning is used for, how to process data, how to cluster, how to reduce your dimensions, and how to reduce the principal components using PCA. It’s time to put all these skills to use by creating an analysis for your clients who are preparing to get into the cryptocurrency market.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

# Deliverables 
* Deliverable 1: Preprocessing the Data for PCA
* Deliverable 2: Reducing Data Dimensions Using PCA
* Deliverable 3: Clustering Cryptocurrencies Using K-means
* Deliverable 4: Visualizing Cryptocurrencies Results

# resources
* Scikit-learn
* Plotly
* hvPlot
* crypto_data.csv

# Deliverable 1 

# requierments: 
Using your knowledge of Pandas, you’ll preprocess the dataset in order to perform PCA in Deliverable 2

* Read in the crypto_data.csv to the Pandas DataFrame named crypto_df.
* Keep all the cryptocurrencies that are being traded.
* Keep all the cryptocurrencies that have a working algorithm.
* Drop the IsTrading column.
* Remove rows that have at least one null value.
* Filter the crypto_df DataFrame so it only has rows where coins have been mined.
* Create a new DataFrame that holds only the cryptocurrency names, and use the crypto_df DataFrame index as the index for this new DataFrame.
* Remove the CoinName column from the crypto_df DataFrame since it's not going to be used on the clustering algorithm.

Take a moment to check that your crypto_df DataFrame looks like the image below:
![image](https://user-images.githubusercontent.com/89880015/149634924-b9d8b58b-9409-41e6-acb8-e56e93199187.png)

* Use the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and store the resulting data in a new DataFrame named X.
* Use the StandardScaler fit_transform() function to standardize the features from the X DataFrame.

results: 

* getting a list of names 
![image](https://user-images.githubusercontent.com/89880015/149635110-de967c0c-1533-42ed-90a6-c070449eaf60.png)

* removing coinName
![image](https://user-images.githubusercontent.com/89880015/149635124-714cc3f4-9566-4a15-984e-8b0f77095d11.png)

* Use the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and store the resulting data in a new DataFrame named X.
![image](https://user-images.githubusercontent.com/89880015/149635164-ee05b68a-f8d6-452f-bd67-d4863bca2076.png)

# Deliverable 2

# requierments
* The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components (10 pt)
![image](https://user-images.githubusercontent.com/89880015/149635644-9e54848d-9b83-43f4-8824-c0fbac7c0e27.png)

* The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame (10 pt)
![image](https://user-images.githubusercontent.com/89880015/149635652-c1743da1-e730-4ea6-9cb6-8e6dfd8c7cec.png)

# Deliverable 3

# requierments

The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:

* An elbow curve is created using hvPlot to find the best value for K (10 pt)
![image](https://user-images.githubusercontent.com/89880015/149635948-4f72c0f6-cb36-47c6-89f2-66773d07b52c.png)

![image](https://user-images.githubusercontent.com/89880015/149635939-e3fb91c4-f787-42ea-b991-1e0ab517fd8d.png)

* Predictions are made on the K clusters of the cryptocurrencies’ data (5 pt)
![image](https://user-images.githubusercontent.com/89880015/149635971-04a803eb-bae7-4d83-82a5-53cc20c9d02c.png)

* A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class (5 pt)
![image](https://user-images.githubusercontent.com/89880015/149636031-af0fed39-6c0e-4387-bd57-eaceb07503bf.png)

# Deliverable 4

# requierments 

* The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover (10 pt)
![image](https://user-images.githubusercontent.com/89880015/149636094-fae1013e-96be-4361-8711-070d8ff8081b.png)

![image](https://user-images.githubusercontent.com/89880015/149636106-f7b22a38-8c7e-45b6-9260-0538c9f5b026.png)

* A table with tradable cryptocurrencies is created using the hvplot.table() function (3 pt)
![image](https://user-images.githubusercontent.com/89880015/149636214-e9853cc2-a749-473e-82a4-d81dc285162b.png)



* The total number of tradable cryptocurrencies is printed (2 pt)
![image](https://user-images.githubusercontent.com/89880015/149636167-460fcb73-fa9f-4ac1-83db-a96ae85c0e4a.png)

* A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns (5 pt)
![image](https://user-images.githubusercontent.com/89880015/149636247-a942eb04-a9cd-4776-8995-b9570bcb08ea.png)


* A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you   hover over the data point (10 pt)
![image](https://user-images.githubusercontent.com/89880015/149636261-219efa65-4e36-465d-836f-ee84f2669553.png)

