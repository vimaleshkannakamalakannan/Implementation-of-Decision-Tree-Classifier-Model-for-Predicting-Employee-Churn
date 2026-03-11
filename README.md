# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Vimalesh kanna MK
RegisterNumber:  212225230303

/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: THARUN DP
RegisterNumber:25018717
# Import required libraries
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.preprocessing import LabelEncoder
from sklearn.metrics import accuracy_score, classification_report

# Load dataset (example CSV file)
data = pd.read_csv("Employee.csv")

# Encode categorical columns
le = LabelEncoder()
data['OverTime'] = le.fit_transform(data['OverTime'])
data['Attrition'] = le.fit_transform(data['Attrition'])

# Select features and target
X = data[['Age', 'MonthlyIncome', 'YearsAtCompany', 'JobSatisfaction', 'OverTime']]
y = data['Attrition']

# Split data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42)

# Create Decision Tree Classifier
dt = DecisionTreeClassifier(criterion='gini', random_state=42)

# Train the model
dt.fit(X_train, y_train)

# Predict the test data
y_pred = dt.predict(X_test)

# Evaluate the model
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))


*/
*/
```

## Output:
<img width="956" height="435" alt="image" src="https://github.com/user-attachments/assets/91aaa425-9a8a-4b4c-ad76-c05c57384c02" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
