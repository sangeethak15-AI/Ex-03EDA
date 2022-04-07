# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1:Create a new file in jupyter notebook.

### STEP 2:Upload the given csv file.

### STEP 3:Write codes for Data Analysis (EDA).

### STEP 4:Plot the result in various formats.

### STEP 5: End the program.

# CODE
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()
sns.displot(df["Age"])
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
```
# OUPUT
![OP1](https://user-images.githubusercontent.com/93992063/162118281-aba68f45-6f2c-489f-8d64-3905aac252c1.png)
![op2](https://user-images.githubusercontent.com/93992063/162118285-a930f33c-bfbf-4301-8fa4-490520abe8d2.png)
![op3](https://user-images.githubusercontent.com/93992063/162118292-f006ce45-30f1-42df-b0a0-0ab8510492ec.png)
![op4](https://user-images.githubusercontent.com/93992063/162118303-e6523102-826d-43d8-87e7-b5b909cba1ae.png)
![op5](https://user-images.githubusercontent.com/93992063/162118314-280ed671-7dba-4774-a43b-7d82482bc542.png)
![op6](https://user-images.githubusercontent.com/93992063/162118329-a65a0591-6556-4de6-b7ed-06859dd92e3f.png)
![op7](https://user-images.githubusercontent.com/93992063/162118334-aa1bbe1a-d030-46e9-a9a8-98c1bbbd6404.png)
![op8](https://user-images.githubusercontent.com/93992063/162118337-c5995abb-9693-456b-b462-4f232e0d1805.png)
![op9](https://user-images.githubusercontent.com/93992063/162118339-f82adb67-c081-423e-b4d2-657ba510f301.png)
