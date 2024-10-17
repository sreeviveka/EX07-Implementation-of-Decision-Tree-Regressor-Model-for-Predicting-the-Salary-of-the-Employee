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
numerical form using label encoding or one-hot encoding. 4. Split the Dataset: Define your features (X) and target (y), then split the data into training and testing sets.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sreeviveka V.S
RegisterNumber:  2305001031
*/
import pandas as pd
data-pd.read_csv("/content/Salary_EX7.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le-LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position", "Level"]]
x.head()
y-data "Salary"]
from sklearn.model selection import train_test split
x_train,x_test,y_train,y_test-train_test_split(x,y, test size=0.2, random_state=2)
from sklearn.tree import Decision TreeRegressor
dt-DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred-dt.predict(x_test)
from sklearn import metrics
mse-metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred) r2
dt.predict([[5,6]])
```

## Output:
![Screenshot 2024-10-17 103008](https://github.com/user-attachments/assets/ccc2a541-e624-414b-b427-4b19348ce632)
![Screenshot 2024-10-17 103015](https://github.com/user-attachments/assets/91fc8437-e471-4401-b744-a2e3e1fe4206)
![Screenshot 2024-10-17 103024](https://github.com/user-attachments/assets/452d8c09-08ad-4bf8-a55d-fc342aac3860)
![Screenshot 2024-10-17 103036](https://github.com/user-attachments/assets/015a3735-5bb3-41ed-953a-c2f1fac83249)
![Screenshot 2024-10-17 103127](https://github.com/user-attachments/assets/98885866-2693-4a5a-9329-5bcab2427a2f)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
