# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the dataset and select input features and target profit.
2. Standardize the input features and initialize weights, bias, and learning rate.
3. Calculate predictions, MSE loss, and update weights and bias using gradient descent.
4. Print final weights and bias, then plot loss versus iterations.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: Joshua Daniel A
RegisterNumber: 212225040161


import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("ex3.xls")

X = data[["R&D Spend", "Administration", "Marketing Spend"]].values 
y = data["Profit"].values


X = (X - np.mean(X, axis=0)) / np.std(X, axis=0)


m, n = X.shape          
w = np.zeros(n)         
b = 0.0
alpha = 0.01             
epochs = 1000

losses = []


for i in range(epochs):
    y_hat = np.dot(X, w) + b

    loss = np.mean((y_hat - y) ** 2)
    losses.append(loss)


    dw = (2/m) * np.dot(X.T, (y_hat - y))
    db = (2/m) * np.sum(y_hat - y)

    
    w = w - alpha * dw
    b = b - alpha * db




print("Final Weights:", w)
print("Final Bias:", b)


plt.plot(losses)
plt.xlabel("Iterations")
plt.ylabel("Loss (MSE)")
plt.title("Loss vs Iterations (Multiple Linear Regression)")
plt.show()

*/
```

## Output:
![linear regression using gradient descent](sam.png)
<img width="795" height="690" alt="ex3 ml graph" src="https://github.com/user-attachments/assets/017ceaa7-d3d3-4671-9d26-f5107b93636e" />

<img width="1191" height="240" alt="ex3 ml" src="https://github.com/user-attachments/assets/c9987617-dc27-401b-840b-7d2fb1364747" />

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.






## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
