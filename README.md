# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import pandas as pd

### Step2
read the csv file

### Step3
get the value of x and y variables

### Step4
create the linear regression model and fit

### Step5
predict the CO2 emission of a car where the weight is 2300kg and the volume is 1300cm3
### Step6
print the predicted output
## Program:
```
# Developed by:YUVARANI T
# Register no:22009033
import pandas as pd
from sklearn import linear_model
import matplotlib.pyplot as plt

df = pd.read_csv("cars.csv")

X = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(X,y)
#Cofficients and intercept of Model
print('Coefficients: ', regr.coef_) 
print('Intercept: ',regr.intercept_)

#predict the CO2 emission of a car where the weight is 300kg, and the volume is 1300cm3:
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume', predictedCO2)


```
## Output:
![MULTI](https://user-images.githubusercontent.com/121418522/214820943-b691581f-ee0f-4478-b6f1-c229d5ed13bc.jpg)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
