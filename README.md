# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required Python libraries such as pandas, sklearn, seaborn, and matplotlib.
2. Load the dataset tumor.csv using pd.read_csv()
3. Display the first few rows of the dataset using data.head(
4. Display the column names using data.columns
5. Separate the features (X) and target variable (y) from the dataset
6. Split the dataset into training set and testing set using train_test_split()
7. Create a Decision Tree Classifier model
8. Train the model using the training data with the fit() method
9. Predict the output for the test data using the predict() method
10. Evaluate the model using accuracy score, classification report, and confusion matrix
11. Visualize the confusion matrix using a Seaborn heatmap and display it using Matplotlib

## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: sri jai.v
RegisterNumber:  25018437
*/
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: SRIJAI V
RegisterNumber:  25018437

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
import seaborn as sns
import matplotlib.pyplot as plt

data = pd.read_csv('tumor.csv')
print(data.head())
print(data.columns)

X = data.drop(columns=['Class']) 
y = data['Class']

X_train, X_test, y_train, y_test = train_test_split(X,y,test_size=0.3, random_state=42)

model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

accuracy = accuracy_score(y_test, y_pred)
print("Classification Report:\n", classification_report(y_test, y_pred))
conf_matrix = confusion_matrix(y_test, y_pred)

print("Name: SRIJAI V")
print("Reg No:25018437")

sns.heatmap(conf_matrix, annot=True, fmt="d", cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix")
plt.show()
*/
```

## Output:


<img width="1421" height="341" alt="Screenshot 2026-03-10 141438" src="https://github.com/user-attachments/assets/ab766339-8c74-49ec-bc5d-484407c8f383" />
<img width="1421" height="847" alt="Screenshot 2026-03-10 141526" src="https://github.com/user-attachments/assets/b04af424-9dbc-4f47-aab8-b7b42ccd399d" />


## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
