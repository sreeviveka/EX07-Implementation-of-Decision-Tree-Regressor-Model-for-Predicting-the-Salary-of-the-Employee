# EX 7 Implementation of Decision Tree Regressor Model for Predicting the Salary of the Employee
## DATE:
## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
 1. Load the Dataset: Import the data (e.g., employee salary data) into a pandas DataFrame.
 2. Handle Missing Values: Identify and either fill or remove missing values.
 3. Encode Categorical Variables: Convert categorical columns (e.g., department, gender) into
 numerical form using label encoding or one-hot encoding.
 4. Split the Dataset: Define your features (X) and target (y), then split the data into training and
 testing sets.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sreeviveka V.S
RegisterNumber:  2305001031
*/
 import pandas as pd
 data=pd.read_csv("/content/Salary_EX7.csv")
 data.head()
 data.info()
 data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
 le=LabelEncoder()
 data["Position"]=le.fit_transform(data["Position"])
 data.head()
 x=data[["Position","Level"]]
 x.head()
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
```

## Output:
![WhatsApp Image 2024-10-17 at 14 09 17_ceb10d11](https://github.com/user-attachments/assets/2f22e1d4-e55e-43b0-ac1e-5024f9fc4b3c)
![WhatsApp Image 2024-10-17 at 14 09 34_3f44c190](https://github.com/user-attachments/assets/20c6377c-acaa-4951-8cdf-d0d529f17568)
![WhatsApp Image 2024-10-17 at 14 09 37_7aa7ae2a](https://github.com/user-attachments/assets/f010e57a-b5e4-4a14-abfd-cd6fbfddee6f)
![WhatsApp Image 2024-10-17 at 14 09 52_771e56ab](https://github.com/user-attachments/assets/a76fc072-dba0-4cd8-b569-45e1f41d8030)
![WhatsApp Image 2024-10-17 at 14 10 53_4e51481d](https://github.com/user-attachments/assets/e9652175-817e-4c96-a61c-6b96a8801d53)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
