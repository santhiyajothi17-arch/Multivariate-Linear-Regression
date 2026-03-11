# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>

### Step2
<br>

### Step3
<br>

### Step4
<br>

### Step5
<br>

## Program:
```
import matplotlib.pyplot as plt
import numpy as np
from sklearn import linear_model
from sklearn.datasets import load_diabetes
from sklearn.model_selection import train_test_split

# Load dataset
data = load_diabetes()
X = data.data
y = data.target

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=1
)

# Model
reg = linear_model.LinearRegression()
reg.fit(X_train, y_train)

print("Coefficients:", reg.coef_)
print("Variance score:", reg.score(X_test, y_test))

plt.scatter(reg.predict(X_train), reg.predict(X_train) - y_train,
            color="green", s=10, label="Train data")

plt.scatter(reg.predict(X_test), reg.predict(X_test) - y_test,
            color="blue", s=10, label="Test data")

plt.hlines(y=0, xmin=0, xmax=400, linewidth=2)

plt.legend(loc="upper right")
plt.title("Residual Errors")
plt.show()

```
## Output:
<img width="1321" height="765" alt="image" src="https://github.com/user-attachments/assets/0db27a42-f484-424f-ada7-189b2c89add9" />
<img width="1314" height="242" alt="image" src="https://github.com/user-attachments/assets/781ea00a-ff7b-4ff7-a804-08ac5067434d" />
<img width="1399" height="729" alt="image" src="https://github.com/user-attachments/assets/49a2aab2-2fd6-4828-b85f-72df6f4f1b02" />


<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
