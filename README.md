# Implementation of Univariate Linear Regression

## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
## Step 1. 
Get the independent variable X and dependent variable Y.
## Step 2.
Calculate the mean of the X -values and the mean of the Y -values.
## Step 3. 
Find the slope m of the line of best fit using the formula. 

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

## Step 4. 
Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

## Step 5. 
Use the slope m and the y -intercept to form the equation of the line.
## Step 6. 
Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Lokesh M
RegisterNumber:  212223230114
*/
import matplotlib.pyplot as plt
import numpy as np

#Preprocessing Input data

X=np.array(eval(input()))
Y=np.array(eval(input()))

#Mean
x_mean=np.mean(X)
y_mean=np.mean(Y)
num=0  #for slope
denom=0 #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-x_mean)*(Y[i]-y_mean)
    denom+=((X[i]-x_mean)**2)

#calculate slope
m=num/denom;

#calculate intercept
b=y_mean-m*x_mean

print(m,b)
#Line equation
y_predicted=m*X+b
print(y_predicted)

#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## Output:
## Slope and Intercept
1.8 0.0
## Y-Predicted
[1.8 3.6 5.4 7.2 9. ]

## Graph:
![image](https://github.com/user-attachments/assets/58c50a89-6366-48e7-954d-044d2f8b13b3)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
