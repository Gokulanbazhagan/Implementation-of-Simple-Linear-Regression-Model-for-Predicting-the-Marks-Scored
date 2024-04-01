# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
```
1.Import the standard Libraries.
2.Set variables for assigning dataset values.
3.Import linear regression from sklearn
4.Assign the points for representing in the graph
5.Predict the regression for marks by using the representation of the graph
6.Compare the graphs and hence we obtained the linear regression for the given datas
```

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: gokularamanan k
RegisterNumber:  2122222300400
*/
import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 df=pd.read_csv('/content/score.csv')
 df.head(10)
 plt.scatter(df['Hours'],df['Scores'])
 plt.xlabel('Hours')
 plt.ylabel('Scores')
 x=df.iloc[:,0:-1]
 y=df.iloc[:,-1]
 from sklearn.model_selection import train_test_split
 X_train,X_test,Y_train,Y_test=train_test_split(x,y,test_size=0.2,random_state=0)
 from sklearn.linear_model import LinearRegression
 lr=LinearRegression()
 lr.fit(X_train,Y_train)
 X_train
 Y_train
 plt.scatter(df['Hours'],df['Scores'])
 plt.xlabel('Hours')
 plt.ylabel('Scores')
 plt.plot(X_train,lr.predict(X_train),color='blue')
 lr.coef_
 lr.intercept_

```

## Output:

1)HEAD:

![image](https://github.com/Gokulanbazhagan/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/119518996/dad33258-b5c6-4e6c-8562-251c64098f85)

2)GRAPH OF PLOTTED DATA:

![image](https://github.com/Gokulanbazhagan/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/119518996/138cf36a-47d8-40fe-960b-a9876ca8abea)

3)TRAINED DATA:

![image](https://github.com/Gokulanbazhagan/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/119518996/957f13d9-19f4-4ca3-9048-756d7fb51b05)

4)LINE OF REGRESSION:
![image](https://github.com/Gokulanbazhagan/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/119518996/59d76d36-f292-4900-8931-5cb394198e33)

5)COEFFICIENT AND INTERCEPT VALUES:
 ![image](https://github.com/Gokulanbazhagan/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/119518996/ab521a6b-05c6-4a96-80a8-6e6fa7abf5ce)






## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
