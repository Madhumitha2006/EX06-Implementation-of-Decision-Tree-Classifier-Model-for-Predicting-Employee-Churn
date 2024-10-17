# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.

2. Handle Missing Values: Identify and fill or drop missing values.

3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data
(e.g., department, gender).

4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and
testing sets.

## Program:
```

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Madhu mitha V
RegisterNumber:  2305002013
import pandas as pd
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv("/content/Employee_EX6.csv")
data=df.copy()
data
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data
x=data.drop(['Departments','left'],axis=1)
y=data['left']
clf=DecisionTreeClassifier()
clf.fit(x,y)
plt.figure(figsize=(80,80))
plot_tree(clf,feature_names=x.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/a77ca489-f877-4cdd-b2f6-c3ecccb28270)
![image](https://github.com/user-attachments/assets/90f69d60-3385-4ff0-98b3-9de9544cafb7)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
