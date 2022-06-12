# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5. Find the accuracy of the model and predict the required values by importing the
6. Required module from sklearn.

## Program:
```
/*
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: MUHAMMED ASHIQ B
RegisterNumber:  212220040094
*/
import pandas as pd
d=pd.read_csv("/content/Employee.csv")
d.head()
d.info()
d.isnull().sum()
d["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
l=LabelEncoder()
d["salary"]=l.fit_transform(d["salary"])
d.head()
x=d[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=d["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
acc=metrics.accuracy_score(y_test,y_pred)
acc
dt.predict([[.5,.8,9,260,6,0,1,2]]) 
*/
```

## Output:
![1 1](https://user-images.githubusercontent.com/104640895/173217685-8fb353de-2d14-46ea-abe9-e9f743541665.png)
![1 2](https://user-images.githubusercontent.com/104640895/173217691-2ace076f-6792-4ae9-a5ae-ae19ae04c885.png)
![1 3](https://user-images.githubusercontent.com/104640895/173217697-09083e0f-ed31-4528-a0d7-fb8adf8fbf5a.png)
![1 4](https://user-images.githubusercontent.com/104640895/173217700-e1ee821c-bba0-496e-822b-317883a85eab.png)
![1 5](https://user-images.githubusercontent.com/104640895/173217703-36ac5af4-afdc-4bc6-a7f1-f3bbd4a898e0.png)
![1 6](https://user-images.githubusercontent.com/104640895/173217712-3959b6ea-78a4-4c77-8163-551876f95aa8.png)
![1 7](https://user-images.githubusercontent.com/104640895/173217715-e9609db6-752d-46b5-8f9b-e0f77f111607.png)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
