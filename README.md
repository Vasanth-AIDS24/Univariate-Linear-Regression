# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
Developed by: Vasanth P
Registeration Number:24900136
import numpy as np
from matplotlib import pyplot
X=np.array(eval(input()))
Y=np.array(eval(input()))
xmean=np.mean(X)
ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
    num+=(X[i]-xmean)*(Y[i]-ymean)
    den+=(X[i]-xmean)**2
slope=num/den
c=ymean-slope*xmean
Y_pred=slope*X+c
pyplot.scatter(X,Y,color='red')
pyplot.plot(X,Y_pred,color='blue')
pyplot.show()
```
## Output
![alt text](image.png)
![alt text](image-1.png)
## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
