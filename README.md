# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages and print the present data. 
2.Print the placement data and salary data.
3.Find the null and duplicate values. 
4.Using logistic regression find the predicted values of accuracy , confusion matrices. 
5.Display the results.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import confusion_matrix, accuracy_score, classification_report

df = pd.read_csv("Placement_Data_Full_Class.csv")

X = df[['ssc_p', 'hsc_p', 'degree_p', 'etest_p', 'mba_p']]
y = df['status'].map({'Not Placed': 0, 'Placed': 1})

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.25, random_state=42
)

scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

model = LogisticRegression()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\nAccuracy Score:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))

new_student = np.array([[70, 75, 70, 80, 65]])

new_student_scaled = scaler.transform(new_student)

placement_pred = model.predict(new_student_scaled)
placement_prob = model.predict_proba(new_student_scaled)

print(f"\nPredicted Placement Status: {'Placed' if placement_pred[0] == 1 else 'Not Placed'}")
print(f"Probability of Placement: {placement_prob[0][1]:.2f}")
Developed by: DARSHIKA M
RegisterNumber:  212225220020
*/
```

## Output:
<img width="1920" height="1080" alt="Screenshot (524)" src="https://github.com/user-attachments/assets/24139afa-619d-49bd-adaf-5c2b2d34ac49" />



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
