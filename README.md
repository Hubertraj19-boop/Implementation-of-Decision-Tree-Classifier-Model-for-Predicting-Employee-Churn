# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. mport required libraries and create the employee dataset using pandas DataFrame.
2.Split the dataset into input features (X) and target variable (Churn), then divide into training and testing sets.
3.Train a Decision Tree Classifier using the training data and predict churn on the test data.
4.Evaluate the model performance using accuracy, confusion matrix, and visualize the decision tree. 
   
   

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Hubert raj.I
RegisterNumber:  25018951
*/
```
```
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
import matplotlib.pyplot as plt
df = pd.DataFrame(data)
X = df[['satisfaction_level',
        'last_evaluation',
        'number_project',
        'average_montly_hours',
        'time_spend_company']]

y = df['left']
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)
model = DecisionTreeClassifier(criterion='entropy', max_depth=5, random_state=42)

model.fit(X_train, y_train)
model = DecisionTreeClassifier(
    criterion='entropy',
    max_depth=3,              
    min_samples_split=50,     
    min_samples_leaf=20,      
    random_state=42
)

model.fit(X_train, y_train)
plt.figure(figsize=(14, 7))

plot_tree(model,
          feature_names=X.columns,
          class_names=['Stayed', 'Left'],
          filled=True,
          rounded=True,
          fontsize=8)

plt.title("Decision Tree for Employee Churn Prediction")
plt.show()
new_emp = [[0.35, 0.55, 3, 160, 3]]

prediction = model.predict(new_emp)

if prediction[0] == 1:
    print("Employee is likely to LEAVE")
else:
    print("Employee is likely to STAY")
```


## Output:
<img width="877" height="101" alt="image" src="https://github.com/user-attachments/assets/fde2413d-533c-4c54-bbe5-7e7f41a30ee8" />
<img width="618" height="340" alt="image" src="https://github.com/user-attachments/assets/9d59a0da-5e06-490d-8c60-d6e1c886ed58" />
<img width="1026" height="506" alt="image" src="https://github.com/user-attachments/assets/468a0f18-72f3-49e9-bd23-e7e1805703f8" />
<img width="393" height="67" alt="image" src="https://github.com/user-attachments/assets/a34abf4a-ce82-4891-b53a-a70a3f780d63" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
