# Customer preferences
## Why we choose "customer's preference" dataset?
### We chose the data set about the customer’s preferences regarding the nature of each store because we have more general information about the business, which makes understanding it better for us than other topics, so we are able to perform better analysis
### We can implement on this dataset many algorithms that we have studied , and obtain results that are understandable and have value to the organization

## Explain the data
### The dataset contain data about 150 store of The FOODmart supermarket chain, which is one of the leading grocery stores in Australia
### The data set describes the nature of each store in terms of sales, Gross profits, location, holidays, home delivery, parking space, number of staff, managers' information and Cost of the basket of food items

## Target of the project
### 1- Analyse the natural of the stores in this super market chain
### 2- Help the company to make informed desicion about making changes in its store
### 3- Identify the customer preferences by analysing the features that improve the store sales 

## Steps to reach our target
### 1- Pre-Processing 
#### 1. Data transformations: In these dataset categorical data as already  encoded to numerical variables 
#### 2. Feature selection: We selected numerical features in dataset and got  insights about these
#### 3. Handle outliers: Display boxplot of numerical variables to detect the outliers and identify outlier with Z_Score and replace it with the feature mean

### 2- Exploratory analysis
#### 1. Display the count of each category using  to detect if there is any an expected values
#### 2. Plotting the store's no. with its sales and wages
#### 3. Display the average cost of the main food basket for each store in 2014 
#### To see the nature of each store

### 3- Algorithms
* Regression
##### Preparing the data for the model:
##### 1. normalize the features using the Min-Max scaler 
##### 2. split the data into train and test 
##### Implement Multiple Linear Regression:
##### Use OLS model to see the impact of " Wages $m, Adv.$m, Competitors, Basket:2014" on the Sales
##### Implement Simple Linear Regression:
##### Use WLS model:
1. To determine how the number of effective staff impact the sales
2. To determine if the number of available car spaces improve the sales 
##### Evaluate the model to detect its performance using:
1. R-Squared
2. Significance of the coefficients
3. MSE
##### Plot the fitted line and errors of each model
##### Used methods:
##### MinMaxScaler(), fit_transform() : rescale the values of a dataset to a specific range between 0:1 to ensure that all features contribute equally to the model's performance. 
##### train_test_split() : split the data into
##### 1. Training set to train the model
##### 2. Test set to evaluate the model's performance
##### With 20% propotion of data for testing the model and the remaining 80% for training 
##### OLS() : apply ordinary least squares multiple regression to show the correlation between specified features with sales
##### fit() : fit the model with training data
##### predict() : predict the results of the model with test data

* Clustering
##### Preparing the data: 
##### 1. Normalizing the numerical features using standard scale to reduce the impact of the large scale features and the impact of the extreme values "outliers"
##### 2. Encode the categorical features using dummy encoding to fit into the model
##### Determine the K value for k-mean algorithm:
##### Applying elbow method and visualize it using yellowbrick library to display the elbow point
##### Use PCA method to reduce dimensionality to improve the clustering and make clear clusters
##### Implement k-means and make column to describe the cluster of each store
##### Extract the characteristics of each cluster and using graphs to compare between them

* Neural Network
##### Multi-Layer Perceptron Neural Network
##### 1- Normalize the numerical features using StandardScaler() because it's stable updates to the network's weight and biases during training and presents improved performance 
##### 2- Encode the categorical featuresSplit data into Train and Test using train_test_split
##### 3- Apply MLP with loss function Mean squared error
##### 4- Using the MLP for make predictions 
##### 5- Evaluate the MLP using: Mean Squared Error, Root Mean Squared Error, R-Squared, Mean absolute error, Explained variance
##### 6- Make predictions on new data and get the predicted sales value
##### 7- Get weight for each feature
##### 8- Calculate the importance of each feature
##### Looking at the importance scores, we can see the effect each feature has on sales

* Association Rule
#### Compare between some features like 
##### * Sales $m and Number of Staff
##### * Sales $m and Car Spaces
##### * Female managers and Advertising
##### * Gross Profit and Competitors

## Insights

### Can get a large number of insights:
### 1- From Regression:
#### 1. The Advertise expenses has the most positive impact compared to " Wages $m, Competitors, Basket:2014" on the sales.
#### 2. The number of effective staff has a high positive impact on the sales with about  increasing the sales by $886800 for a unit.
#### 3. The available car spaces also have high positive impact on the sales as it will increase by about $646300 for unit.
- 
### 2- From clustering:
#### 1. cluster 0 has the higher gross profit this can help to detect features to improve other clustering as offering home delivery services.
#### 2. stores that assigned to cluster 1 have high features and the company can use its strategies to improve the other stores.
#### 3. cluster 2 stores have the lower features and need more attention from the company managers. they can improve some of its feature and change its managers to more experience ones.

### 3- From Neural Network:
#### 1. neural network has performed reasonably well, with a relatively low MSE, RMSE,MAE and MAPE and with high Explained variance
#### 2. This model can be used to predict sales of store with specific characteristics, and help the supermarket chain to make informed decision about opening a new store

### 4- From Association Rule:
#### 1. The Sales and the number of effective staff are strongly related and have Mutual effect on each other
#### 2. Sales and the number of available parking space are strongly related
#### 3. The stores with female managers are more likely to have low advertising expenses. 
#### 4. Expected stores with high number of competing supermarkets have low profit

### Customers prefer stores with :

#### 1. large parking spaces
#### 2. high number of full time staff
#### 3. low prices of main basket items
#### 4. Home delivery
#### 5. Opens on Sundays
