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
import pandas as pd
from sklearn import linear_model, metrics
from sklearn.model_selection import train_test_split

data_url = "http://lib.stat.cmu.edu/datasets/boston"
raw_df = pd.read_csv(data_url, sep="\s+", skiprows=22, header=None)

data = np.hstack([raw_df.values[::2, :], raw_df.values[1::2, :2]])
target = raw_df.values[1::2, 2]

X = data
y = target


X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=1
)


reg = linear_model.LinearRegression()


reg.fit(X_train, y_train)

print('Coefficients: \n', reg.coef_)

print('Variance score: {}'.format(reg.score(X_test, y_test)))

plt.style.use('fivethirtyeight')


plt.scatter(reg.predict(X_train), reg.predict(X_train) - y_train,
            color="green", s=10, label='Train data')


plt.scatter(reg.predict(X_test), reg.predict(X_test) - y_test,
            color="blue", s=10, label='Test data')


plt.hlines(y=0, xmin=0, xmax=50, linewidth=2)

plt.legend(loc='upper right')
plt.title("Residual errors")
plt.show()

```
## Output:
<img width="1321" height="765" alt="image" src="https://github.com/user-attachments/assets/6c994523-68a5-451c-98df-cb4ce2bd10e3" />
<img width="1314" height="242" alt="image" src="https://github.com/user-attachments/assets/885f0926-e6ce-4df1-9097-b58c43d09f39" />
<img width="1399" height="729" alt="image" src="https://github.com/user-attachments/assets/861f927d-20e5-42b4-beda-7e6090016ab5" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
