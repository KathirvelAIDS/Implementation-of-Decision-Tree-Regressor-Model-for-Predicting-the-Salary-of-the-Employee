# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Import pandas library to read csv or excel file. 

Import LabelEncoder using sklearn.preprocessing library.

Transform the data's using LabelEncoder.

Import decision tree regressor from sklearn.tree library to predict the values.

Find Mean squared error and r2

Predict the values.

End of the program

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: kathirvel.A
RegisterNumber: 212221230047 
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

Output:




Initial dataset:


![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/e67dce43-f2f1-4b10-aa93-13b19af72c40)




Data Info:

![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/27a4e4fe-3c91-4fe9-aadb-3feaa6c6964c)



Optimization of null values:


![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/d6f95ced-aafb-462c-ad5c-c2df1bdc3172)




Converting string literals to numericl values using label encoder:


![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/c73a0f0f-eee7-4f34-988e-4770934cf60e)




Assigning x and y values:

![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/d863d9b4-6b6a-4bda-aa85-b0bc7dbbe2d3)



Mean Squared Error:

![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/166fe836-2adc-4a17-bb9d-75e8fe732dba)



R2 (variance):


![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/f3d52247-a3d4-4e08-9aab-f5d3d645d505)


Prediction:


![image](https://github.com/KathirvelAIDS/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94911373/c9cd2459-95e0-433e-8d09-313221422e9b)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
