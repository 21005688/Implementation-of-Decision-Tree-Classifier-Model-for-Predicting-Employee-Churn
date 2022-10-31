# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries .
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply decision tree Classifier on to the dataframe.
7. Get the values of accuracy and data prediction. 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: J.DEEPIKA
RegisterNumber: 212221230016

import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:

![AA](https://user-images.githubusercontent.com/94747031/199072026-c0e8bfe2-c1a5-434c-b70d-f6ad1974d2b6.png)

![BB](https://user-images.githubusercontent.com/94747031/199072037-5dfb74b4-7104-4e52-95d7-26ae172224c7.png)

![CC](https://user-images.githubusercontent.com/94747031/199072042-48800faf-0e7e-4bd2-9d8c-cf121e0c4e92.png)

![DD](https://user-images.githubusercontent.com/94747031/199072043-416ff1c2-e28e-4608-b4bd-4d7b490ad81e.png)

![EE](https://user-images.githubusercontent.com/94747031/199072045-c68c0f76-d0aa-4893-ad26-d3816e64980c.png)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
