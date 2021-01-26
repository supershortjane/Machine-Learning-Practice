# Pima Indians Diabetes prediction</br> (Logistic Regression)
## 1.Dataset
The data contain diagnostic measurements related with diabetes. The following is the description of each column.

● Pregnancies - Number of times pregnant</br>
● Glucose - Plasma glucose concentration a 2 hours in an oral glucose tolerance test</br>
● BloodPressure - Diastolic blood pressure (mm Hg)</br>
● SkinThickness - Triceps skin fold thickness (mm)</br>
● Insulin- 2-Hour serum insulin (mu U/ml)</br>
● BMI - Body mass index (weight in kg/(height in m)^2)</br>
● DiabetesPedigreeFunction - Diabetes pedigree function</br>
● Age- Age (years)</br>
● label- Class variable(0 or 1) (years)


## 2.Goal
Our goal in this analysis is to predict whether a patient has diabetes or not.


## 3.Overview of Analysis
```
1.Data Preprocessing
2.Model Building
3.Evaluation
```

### Data Preprocessing
There are 9 columns and 768 instances in this dataset, which has no any null values.</br>
No catagorical column in the dataset, so it's no need to do one hot encoding or label encoding.</br>

### Model Building
#### 1.Split data
In our target variable, 500 instances are 0 and 268 instances are 1. 
I split the data into two groups, 70% for training and 30% for testing.</br>
#### 2.Standardization
All the columns are collected in different measuremnts, thus it is better to do standardization to have the columns on a simliar scale.</br>
#### 3.Apply Logistic Regression Model
Our objective is to predict if a person have diabetes. In this practice, I choose Logistic regression as my model.</br>
#### 4.Use Cross-Validation To Make Prediction
The data is tiny, if we use part of data as our testing data, it is possible that we get target variable that is all 0. 
This will result a poor performance. To avoid the problem, I use k-fold cross validation to split my data into k group. And 
for each group, take the group as testing set and take the rest as training set then run the model.
### Evaluation
We elvaluate our model using accuracy(which is the mean of accuracy of the model that we run in k-fold validation) and cofusion matrix.

