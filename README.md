<img width="408" alt="image" src="https://github.com/MOHAMEDRIDWAN/Univariate-Linear-Regression/assets/146993368/e48d0969-29d7-4d1c-8677-1d3932685fdd"># Implementation of Univariate Linear Regression
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
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: Mohamed Ridwan A
#register number: 23003133

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
</br>
<img width="498" alt="Screenshot 2023-12-22 000513" src="https://github.com/MOHAMEDRIDWAN/Univariate-Linear-Regression/assets/146993368/fb5d97d3-e24c-4a8d-933f-6fe4bc6bbdd6">

</br>
<img width="484" alt="Screenshot 2023-12-22 000532" src="https://github.com/MOHAMEDRIDWAN/Univariate-Linear-Regression/assets/146993368/41eaad46-72ff-43d9-926c-b74acfce9eb2">

</br>
<img width="408" alt="Screenshot 2023-12-22 000545" src="https://github.com/MOHAMEDRIDWAN/Univariate-Linear-Regression/assets/146993368/26bfe318-9537-4ef2-89be-ce6a91492be5">

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
