# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: VIJAY K
RegisterNumber: 24901153
import numpy as np
import matplotlib.pyplot as plt

# Input for X and Y as arrays
X = np.array(eval(input("Enter the values for X (as a list): ")))
Y = np.array(eval(input("Enter the values for Y (as a list): ")))

# Calculating the mean of X and Y
X_mean = np.mean(X)
Y_mean = np.mean(Y)

# Initializing numerator and denominator for the slope calculation
num = 0
denom = 0

# Calculating the slope (m)
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    denom += (X[i] - X_mean) ** 2
m = num / denom

# Calculating the intercept (b)
b = Y_mean - m * X_mean

# Predicting Y values using the linear regression equation
Y_predicted = m * X + b

# Output the predicted values
print("Predicted Y values:", Y_predicted)

# Plot the original data points
plt.scatter(X, Y)

# Plot the linear regression line
plt.plot(X, Y_predicted, color='red')


# Output the slope and intercept
print("Slope (m):", m)
print("Intercept (b):", b)

# Display the plot
plt.show() 
*/
```

## Output:
Enter the values for X (as a list): 8,2,11,6,5,4,12,9,6,1
Enter the values for Y (as a list): 3,10,3,6,8,12,1,4,9,14
Predicted Y values: [ 5.22972973 11.86824324  1.91047297  7.44256757  8.54898649  9.65540541
  0.80405405  4.12331081  7.44256757 12.97466216]
Slope (m): -1.1064189189189189
Intercept (b): 14.08108108108108
![best f![Screenshot (2)](0b3dad)
it line](sam.png)
![Screenshot (2)](https://github.com/user-attachments/assets/99dd6e09-6184-45ca-9e4b-26213f209630)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
