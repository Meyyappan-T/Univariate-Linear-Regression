# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
#### Step 1.	Start
#### Step 2.	Get the independent variable X and dependent variable Y and	Calculate the mean of the X -values and the mean of the Y -values.
#### Step 3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
#### Step 4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
#### Step 5.	Use the slope m and the y -intercept to form the equation of the line.
#### Step 6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
#### Step 7. Stop
## Program
```py
#Program developed by:Meyyappan.T
#Register no:212223240086
import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))

X_mean=np.mean (X)
Y_mean=np.mean (Y)
num=0
denom=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denom+=(X[i]-X_mean)**2
m=num/denom
c=Y_mean-m*X_mean
print (m, c)
Y_pred=m*X+c
print (Y_pred)
plt.scatter (X, Y, color='red') 
plt.plot(X,Y_pred,color='black')
plt.show()
```
## Output
![image](https://github.com/Meyyappan-T/Univariate-Linear-Regression/assets/128804366/b8d1f389-7b64-43e3-b69d-b457047cbf7f)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
