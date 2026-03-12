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
import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()





```
## Output
<img width="873" height="213" alt="Screenshot 2026-03-12 083933" src="https://github.com/user-attachments/assets/28b42e41-c4b4-4c3c-892e-5f6db88074bd" />
<img width="947" height="543" alt="Screenshot 2026-03-12 083942" src="https://github.com/user-attachments/assets/33963fb9-e91b-43a7-a9a5-2ec27693bd40" />
<img width="1489" height="587" alt="Screenshot 2026-03-12 140607" src="https://github.com/user-attachments/assets/5cfc8003-344f-429c-82a7-e396ce4e3bf6" />
<img width="1350" height="60" alt="Screenshot 2026-03-12 140617" src="https://github.com/user-attachments/assets/c7f065dd-65cb-487c-bb1b-fc24f4be9472" />
<img width="1038" height="703" alt="image" src="https://github.com/user-attachments/assets/92f77f95-30e4-4ea6-ba4b-126174438720" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.











.









.
