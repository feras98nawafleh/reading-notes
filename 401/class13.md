# Linear Regression
## What is it?
it's a DS/ML technique bases on mathmatical equation where it takes a sample of data and plot a line accros it to decide what of the data is closer to the best value needed and how several variables are related.
## Formula
𝑓(𝐱) = 𝑏₀ + 𝑏₁𝑥₁ + ⋯ + 𝑏ᵣ𝑥ᵣ

where:
<br>
Y: dependent variable
<br>
X: set of independent variables 𝐱 = (𝑥₁, …, 𝑥ᵣ)
<br>
𝛽₀, 𝛽₁, …, 𝛽ᵣ: the regression coefficients
<br>
𝜀: the random error

## Simple Linear Regression
![Linear Regression](https://files.realpython.com/media/fig-lin-reg.a506035b654a.png)

## Code Samples:
```python
# importing required libraries
import numpy as np
from sklearn.linear_model import LinearRegression

# providing data
x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
y = np.array([5, 20, 14, 32, 22, 38])

# showing data
>>> print(x)
[[ 5]
 [15]
 [25]
 [35]
 [45]
 [55]]
>>> print(y)
[ 5 20 14 32 22 38]

# Create a model and fit it
model = LinearRegression()
model.fit(x, y)

# or model = LinearRegression().fit(x, y)

>>> y_pred = model.predict(x)
>>> print('predicted response:', y_pred, sep='\n')
predicted response:
[ 8.33333333 13.73333333 19.13333333 24.53333333 29.93333333 35.33333333]
