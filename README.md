# EXP NO 2

### NAME : KRISHNA KUMAR R
### REG NO : 212223230107

## AIM:
      To perform Exploratory Data Analysis on the given data set.
      
## EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
## ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
![Screenshot 2024-09-27 154959](https://github.com/user-attachments/assets/af499df8-d629-41d8-b6ae-8af3ef93b71f)

```
df.info()
```
![Screenshot 2024-09-27 155018](https://github.com/user-attachments/assets/b2ccd46a-2b14-44f6-bc30-7492a19e111e)

```
df.shape
```
![Screenshot 2024-09-27 155027](https://github.com/user-attachments/assets/108a3a61-2667-4f3f-8094-c56cb0ee999b)

```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.set_index("PassengerId",inplace=True)
print(df.set_index)
```
![Screenshot 2024-09-27 155142](https://github.com/user-attachments/assets/01fd6d6d-3914-4b3f-baf2-ae74eaa545fe)

```
df.describe()
```
![Screenshot 2024-09-27 155155](https://github.com/user-attachments/assets/cb4790cb-8e80-4a7d-ae24-c39ff5cfd6aa)

```
df.nunique()
```
![Screenshot 2024-09-27 155204](https://github.com/user-attachments/assets/915032cf-730c-42ca-8fe6-309f052730cc)

```
df["Survived"].value_counts()
```
![Screenshot 2024-09-27 155211](https://github.com/user-attachments/assets/8f8a9142-d653-479b-b886-c8f7b751d6a2)

```
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![Screenshot 2024-09-27 155218](https://github.com/user-attachments/assets/baf39904-b52e-41be-97cf-1c138a48a77e)

```
sns.countplot(data=df,x="Survived")
```
![Screenshot 2024-09-27 155225](https://github.com/user-attachments/assets/0e8bcc07-f9c1-4a78-8e83-30be6a405a95)

```
df
```
![Screenshot 2024-09-27 155241](https://github.com/user-attachments/assets/e7df57b6-818c-4fb2-910f-22790ce3ca80)

```
df.Pclass.unique()
```
![Screenshot 2024-09-27 155250](https://github.com/user-attachments/assets/357e0e04-8cc1-4ef4-b295-6a22c4870320)

```
df.rename(columns={'sex':'Gender'},inplace=True)
df
```
![Screenshot 2024-09-27 155305](https://github.com/user-attachments/assets/d2703a15-d8cb-43c7-a537-3ae262bdaa44)

```
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
sns.catplot(x="Sex",col='Survived',kind="count",data=df,height=5, aspect=.7)
```
![Screenshot 2024-09-27 155321](https://github.com/user-attachments/assets/084fe349-75c0-49e1-8053-7ae6706d060c)

```
sns.catplot(x='Survived',hue='Sex',data=df,kind='count')
```
![Screenshot 2024-09-27 155332](https://github.com/user-attachments/assets/cc460791-b58c-4013-83a9-b72cce9a0c72)

```
df.boxplot(column='Age',by="Survived")
```
![Screenshot 2024-09-27 155344](https://github.com/user-attachments/assets/135547ea-9600-47cd-81e6-a62a7e86cdfc)

```
sns.scatterplot(x=df['Age'],y=df["Fare"])
```
![Screenshot 2024-09-27 155354](https://github.com/user-attachments/assets/ff7ae0d0-6fa9-4265-bbc2-e15122cc0f27)

```
import matplotlib.pyplot as plt
fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)
```
![Screenshot 2024-09-27 155405](https://github.com/user-attachments/assets/441377af-b8ee-49c4-ad34-8ade176e8cc3)

```
sns.catplot(data=df,col='Survived',x='Sex',hue='Pclass',kind='count')
```
![Screenshot 2024-09-27 155425](https://github.com/user-attachments/assets/900df029-316e-4c6b-9c74-93b7b12431fb)

```
import seaborn as sns
corr=df.corr()
sns.heatmap(corr,annot=True)
```
![Screenshot 2024-09-27 155945](https://github.com/user-attachments/assets/d20f4b12-912b-44be-8318-eb2097291c7a)

```
sns.pairplot(df)
```
![download](https://github.com/user-attachments/assets/ebc6a681-80af-44f4-b007-41099399b2bb)


# RESULT
     Code are sucessfully executed.
