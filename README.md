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

Find Mean squared error and r2.

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
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
*
*/
```

## Output:

data.head()

![image](https://user-images.githubusercontent.com/94911373/169984750-b157da9d-7e46-4a7b-a81f-6a94c943668e.png)


data.info()

![image](https://user-images.githubusercontent.com/94911373/169984837-b5f9b140-de62-493a-b95c-1a35e8151fc0.png)


data.head() using label encoder


![image](https://user-images.githubusercontent.com/94911373/169984891-510bc1e5-02a5-4ef4-985c-09364fc7d986.png)

MSE

![image](https://user-images.githubusercontent.com/94911373/169984956-1a502faf-897b-4e84-bdfd-d0e900fba9fb.png)


r2

![image](https://user-images.githubusercontent.com/94911373/169985024-962991f1-bc58-4f8f-b423-fdba713bb31d.png)


PREDICTION

![image](https://user-images.githubusercontent.com/94911373/169985129-0c24d0bf-b8b1-4afe-8ac9-ffc725f4b1a4.png)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
