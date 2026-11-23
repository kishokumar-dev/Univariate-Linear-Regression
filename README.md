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
#Name:Kishore Kumar P
#Reg num : 26002452
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()






```
## Output
</br><img width="1088" height="628" alt="Screenshot 2026-11-23 195030" src="https://github.com/user-attachments/assets/23b657f9-263e-4c87-8a9a-6c61c48d306b" />

</br><img width="977" height="611" alt="Screenshot 2026-11-23 195039" src="https://github.com/user-attachments/assets/542824d6-122b-4f52-be3b-cf3ebd39c96b" />

</br><img width="1007" height="562" alt="Screenshot 2026-11-23 195229" src="https://github.com/user-attachments/assets/19f8b0f3-e356-4e2b-8bd0-11ca30daadd4" />



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
