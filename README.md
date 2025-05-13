# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset.

3.Check for any null values using the isnull() function.

4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S KANUSHA SREE
RegisterNumber:  212224040149
*/
```

```
import pandas as pd
df=pd.read_csv("/content/Salary.csv")
df.head()
df.info()
df.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()
```
```
x=df[['Position','Level']]
x.head()
y=df['Salary']
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
```
```
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
```
```
dt.predict([[5,6]])
```
## Output:
![image](https://github.com/user-attachments/assets/7f134172-5a95-4d73-bf09-4b1310f882c9)

![image](https://github.com/user-attachments/assets/fb558ee8-53d8-4a3a-8c17-7540f44c5f32)

![image](https://github.com/user-attachments/assets/24e95549-9adf-42d6-8e85-6a57dcf381ec)

![image](https://github.com/user-attachments/assets/4df1d6a5-b4b0-4dbb-94e2-e9e681de5df9)

![image](https://github.com/user-attachments/assets/37af0517-15f0-4a09-8d92-b7503eafde0f)

![image](https://github.com/user-attachments/assets/c600d58f-f823-4905-baf9-e0aa0f935490)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
