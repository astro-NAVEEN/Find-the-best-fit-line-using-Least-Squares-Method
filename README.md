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

"""
Program to implement Univariate Linear Regression
to fit a straight line using Least Squares.

Developed by:
Register Number:
"""

import numpy as np
import matplotlib.pyplot as plt

# Sample Data
X = np.array([1, 2, 3, 4, 5, 6])
Y = np.array([2, 4, 5, 4, 5, 7])

# Mean of X and Y
mean_x = np.mean(X)
mean_y = np.mean(Y)

# Calculate slope (m)
m = np.sum((X - mean_x) * (Y - mean_y)) / np.sum((X - mean_x) ** 2)

# Calculate intercept (b)
b = mean_y - m * mean_x

# Predicted values
Y_pred = m * X + b

# Display equation
print("Slope (m) =", m)
print("Intercept (b) =", b)
print("Equation of Best Fit Line:")
print(f"Y = {m:.2f}X + {b:.2f}")

# Plotting
plt.scatter(X, Y, color='blue', label='Data Points')
plt.plot(X, Y_pred, color='red', linewidth=2, label='Best Fit Line')
plt.title("Univariate Linear Regression")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.grid(True)
plt.show()

## Output:

Slope (m) = 0.8
Intercept (b) = 2.0
Equation of Best Fit Line:
Y = 0.80X + 2.00

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
