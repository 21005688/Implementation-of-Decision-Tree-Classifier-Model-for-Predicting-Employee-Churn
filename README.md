# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries .
2.Read the data frame using pandas.
3.Get the information regarding the null values present in the dataframe.
4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5.Determine training and test data set.
6.Apply decision tree Classifier on to the dataframe.
7.Get the values of accuracy and data prediction. 

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
INITIAL DATAFRAME :
![1](https://user-images.githubusercontent.com/94747031/198823224-7ca2d402-5bba-4a42-be08-64de68bceb2d.png)
CHECKING FOR NULL VALUES:
![2](https://user-images.githubusercontent.com/94747031/198823241-425ea86c-471c-4ccb-a216-6a14d1cb64a4.png)
APPLING LABEL ENCODER:
![3](https://user-images.githubusercontent.com/94747031/198823266-b3f1c4b7-12f1-4dae-b922-a819c28ed32b.png)
![4](https://user-images.githubusercontent.com/94747031/198823276-41534147-7cad-443c-ace1-024d743400a9.png)
ACCUARCY:
![5](https://user-images.githubusercontent.com/94747031/198823290-6c52dc99-b0a0-4513-938f-1f81f9d66eed.png)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
