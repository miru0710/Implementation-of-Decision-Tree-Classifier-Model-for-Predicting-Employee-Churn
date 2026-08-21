# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the employee dataset.

2. Convert categorical data into numerical values and split the data into training and testing sets.

3.Create and train the Decision Tree Classifier using the training data.

4.Predict employee churn using the test data and calculate the accuracy.

5.Display the decision tree and the model accuracy.
 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:MIRUDHULA.N 
RegisterNumber: 212225220063
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score
data = pd.read_csv(r"C:\ml\Employee.csv")
data = pd.get_dummies(data, drop_first=True)
X = data.iloc[:, :-1]
y = data.iloc[:, -1]
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
plt.figure(figsize=(20,10))

plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.show()
*/
```

## Output:
<img width="1372" height="711" alt="image" src="https://github.com/user-attachments/assets/11679698-cf23-4bca-b07f-e5765e7cf436" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
