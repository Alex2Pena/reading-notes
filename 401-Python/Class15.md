# Linear Regression
### Types:
**Simple linear regression**
1 dependent variable (interval or ratio), 1 independent variable (interval or ratio or dichotomous)

**Multiple linear regression**
1 dependent variable (interval or ratio) , 2+ independent variables (interval or ratio or dichotomous)

**Logistic regression**
1 dependent variable (dichotomous), 2+ independent variable(s) (interval or ratio or dichotomous)

**Ordinal regression**
1 dependent variable (ordinal), 1+ independent variable(s) (nominal or dichotomous)

**Multinomial regression**
1 dependent variable (nominal), 1+ independent variable(s) (interval or ratio or dichotomous)

**Discriminant analysis**
1 dependent variable (nominal), 1+ independent variable(s) (interval or ratio)

### Simple Linear Regression With scikit-learn

There are **five** basic steps when implementing linear regression:

1. Import the packages and classes you need.
```
import numpy as np
from sklearn.linear_model import LinearRegression
```
2. Provide data to work with and eventually do appropriate transformations.
```
x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
y = np.array([5, 20, 14, 32, 22, 38])
```
```
>>> print(x)
[[ 5]
 [15]
 [25]
 [35]
 [45]
 [55]]
>>> print(y)
[ 5 20 14 32 22 38]
```
3. Create a regression model and fit it with existing data.
```
model = LinearRegression()
```
**fit_intercept** is a Boolean (True by default) that decides whether to calculate the intercept 𝑏₀ (True) or consider it equal to zero (False).
**normalize** is a Boolean (False by default) that decides whether to normalize the input variables (True) or not (False).
**copy_X is a Boolean** (True by default) that decides whether to copy (True) or overwrite the input variables (False).
**n_jobs** is an integer or None (default) and represents the number of jobs used in parallel computation. None usually means one job and -1 to use all processors.
> model = LinearRegression().fit(x, y)

4. Check the results of model fitting to know whether the model is satisfactory.
*You can obtain the coefficient of determination (𝑅²) with **.score()** called on model:*
```
>>> r_sq = model.score(x, y)
>>> print('coefficient of determination:', r_sq)
coefficient of determination: 0.715875613747954
```
```
>>> print('intercept:', model.intercept_)
intercept: 5.633333333333329
>>> print('slope:', model.coef_)
slope: [0.54]
```
```
>>> new_model = LinearRegression().fit(x, y.reshape((-1, 1)))
>>> print('intercept:', new_model.intercept_)
intercept: [5.63333333]
>>> print('slope:', new_model.coef_)
slope: [[0.54]]
```
5. Apply the model for predictions.
*When applying .predict(), you pass the regressor as the argument and get the corresponding predicted response.*
```
>>> y_pred = model.predict(x)
>>> print('predicted response:', y_pred, sep='\n')
predicted response:
[ 8.33333333 13.73333333 19.13333333 24.53333333 29.93333333 35.33333333]
```
```
>>> x_new = np.arange(5).reshape((-1, 1))
>>> print(x_new)
[[0]
 [1]
 [2]
 [3]
 [4]]
>>> y_new = model.predict(x_new)
>>> print(y_new)
[5.63333333 6.17333333 6.71333333 7.25333333 7.79333333]
```
*Here .predict() is applied to the new regressor x_new and yields the response y_new. This example conveniently uses arange() from numpy to generate an array with the elements from 0 (inclusive) to 5 (exclusive), that is 0, 1, 2, 3, and 4.*



