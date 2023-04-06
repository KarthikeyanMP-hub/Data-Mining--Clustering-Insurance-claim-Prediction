
# Data Mining Project
## Problem 1 Clustering
## Problem Statement
A leading bank wants to develop a customer segmentation to give
promotional offers to its customers. They collected a sample that
summarizes the activities of users during the past few months.
You are given the task to identify the segments based on credit
card usage.

## Problem 2:Prediction of Insurance claim(CART-RF-ANN)
An Insurance firm providing tour insurance is facing higher claim
frequency. The management decides to collect data from the past few
years. You are assigned the task to make a model which predicts the
claim status and provide recommendations to management. Use
CART, RF & ANN and compare the models' performances in train
and test sets.


## Problem 1
## Description of Dataset
The given dataset contains details about 210 customer’s credit card usage data.The data contains details on variables such as spending,advance_payments,probability of full payments,current_balance ,creditlimit,Min_payment_amt,Max_spent_in_single_shopping. All these variables are of float datatype.

### 1.EDA
### Dataset info
The dataset has 210 rows and 7 columns.The columns are of float datatype.
### 2.Descriptive Summary
Pandas describe() can provide a quick summary of the data set as outlined in the notebook.  The output of pandas describe(include="all") is shown below. Here, all columns of the DataFrame are included in the analysis.
#### The average amount spent by customers is14.35 (in thousands).
#### A customer pays 14.32 (in hundreds) as advance on an average.
#### The average probability of customer paying full payment is 0.87.
#### TheCurrent balance maintained by customers range between 4.89 to 6.67 (inthousands).
#### The average credit card limit of customer is 3.23(in thousands).
#### The maximum amount spent in single shopping is 6.55(in 1000s)

### No. of Missing values
The dataset has no missing values.

### 3.Variable analysis
The variables are plotted in different plots to carryout univariate & Bi-variate.The distribution of the variables are studied using Histogram.The Boxplots are used to detect the outliers.The correlation between the variables are studied using pairplot and correlation plot.

### 4.Data Transformation
The dataset is transformed using Z-scale method,as clustering techniques use distance as metric to group the data into various clusters.

### 5.Clustering
#### Hierarchical Clustering
Agglomerative clustering is done on the dataset.The Dendrogram is created to visualize the clusters.Here the dataset is splitted into 3 clusters.
#### K-means Clustering
k-means clustering is the most used non-hierarchical clustering technique. It aims to partition n observations into k clusters. It minimizes within-cluster variances (squared Euclidean distances).
Here the optimal clusters are identified as 3 base on Elbow curve.These clusters are validated by using silscore and Minimum silwidth.

### Cluster Profiling
Based on K-means clustering
Cluster 0 contains 71 user records,Cluster 1 contains 67 user records & Cluster 2 contains 72 user records.
#### Cluster 0 :Medium Spending Group
Good track of maintaining their credit score.
They make purchases and their probability of making full payment to the bank is also good.
#### Recommendations
They can be encouraged to make purchases by offering incentives like cashback offers and other rewards by clubbing with other consumer brands.
We can also increase their credit limit.

#### Cluster 1 :High Spending Group
Most potential customers.They Spend higher compared to others.
The maximum max spent in single shopping is also higher.
#### Recommendations
They can be incentivized by offering best deals from luxury consumer brands.
Special rewards can be offered in form of loyalty points.
Their credit limit can be further increased to encourage them to make frequent purchases.

#### Cluster 2 : Low Spending Group
These customers shown less probability of making full payments
comparatively.The variable ‘Claimed’ is dependent variable and all other variables are independent variables.

#### Recommendations
The payment due reminders should be made frequently to improve their repayment rate and their credit score.
Rewards can be announced to the customers making repayment on time.
These customers spend less than customers in other clusters.Special deals and discounts can be given in categories like grocery and utilities to make them transact frequent.

## Problem 2
## Description of Dataset
The given dataset contains details about 3000 customer’s insurance details.The dataset has 10 variables in which 6 variables are of object type,2 are of integer type and 2 are of float type.

### 1.EDA
### Dataset info
The dataset has 3000 rows and 10 columns.There are no missing values in the dataset.
### 2.Descriptive Summary
Pandas describe() can provide a quick summary of the data set as outlined in the notebook.  The output of pandas describe(include="all") is shown below. Here, all columns of the DataFrame are included in the analysis.
#### From the descriptive stats it is evident that the average age of clients is 38.09.
#### The average commission received by firms is 4.63% of sales. 
#### The average amount worth of sales per customer in procuring tour insurance policies in rupees (in 100’s) is 33.00.

### 3.Variable analysis
The variables are plotted in different plots to carryout univariate & Bi-variate analysis.The distribution of the variables are studied using Histogram.The Boxplots are used to detect the outliers.The correlation between the variables are studied using pairplot and correlation plot.

### 4.Data split
The data is split into train and test set in the ratio of 70:30.

### 5.Classification Models
The following classification models are built to predict the dependent variable.
1.CART Model
2.Random Forest
3.Artificial Neural Network.

### 6.Model Evaluation method
Model Performance Measures are evaluated and compared.
a. Accuracy – How accurately / cleanly does the model classify the
data points. Lesser the false predictions, more the accuracy
b. Sensitivity / Recall – How many of the actual True data points areidentified as True data points by the model . Remember, False
Negatives are those data points which should have been identified
as True.
c. Specificity – How many of the actual Negative data points are
identified as negative by the model
d. Precision – Among the points identified as Positive by the model,how many are really Positive
are evaluated and compared.

The ROC curve is plotted and the AUC score is calculated.

With a recall of 0.50 for test data and accuracy of 0.76 the CART Model is considered as the best model .