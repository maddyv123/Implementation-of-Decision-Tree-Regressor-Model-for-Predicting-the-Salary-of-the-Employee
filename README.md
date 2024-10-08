# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

step 1.start the program.

step 2.Import pandas. 

step 3.Import Decision tree classifier.

step 4.Fit the data in the model.

step 5.Find the accuracy score.

step 6.stop the program.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MATHAVAN V
RegisterNumber: 212223110026
```
```
import pandas as pd
data=pd.read_csv("salary.csv")
data.head()
data.info()
data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
data.info()
x=data[["Position","Level" ]]
x.head()
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
## df.head()
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/f980925b-9858-4699-b49a-1bc54c67d498)
## df.info()
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/06bcc021-d2b2-430b-ae5f-557d5e85a5d1)
## df.isnull.sum()
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/dcc106ed-f9b3-4941-9406-6f7ae97f5d1e)
## after label encoding
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/00608f8d-2cf1-43e7-b6a0-7fef650ce2c6)
## x_train.shape
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/e42cc80c-78d2-4e6c-a2b1-fdd9cc9c981b)
## y_pred
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/8ef76d2a-3c84-45af-bf32-812c29eb43b5)
## MSE value
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/0055942f-979c-4e0e-acde-a9d71e9d78c0)
## R2 value
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/b2ff7fef-1cce-445e-ab95-c68257fa246d)
## predicted value
![image](https://github.com/Mythilidharman/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119104110/334f8a4c-70c0-42b8-af1a-7fb7f94047f1)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
