# Intro to Data Science with Pandas:
pandas is a software library written for the Python programming language for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series.

**importing pandas:**
Customarily, we import as follows:
```python
import numpy as np

import pandas as pd
```
**Creating a Series by passing a list of values, letting pandas create a default integer index:**
```python
s = pd.Series([1, 3, 5, np.nan, 6, 8])

s
Out[4]: 
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64
```

What Can Pandas Do?
Pandas gives you answers about the data. Like:

Is there a correlation between two or more columns?
What is average value?
Max value?
Min value?
Pandas are also able to delete rows that are not relevant, or contains wrong values, like empty or NULL values. This is called cleaning the data.

Where is the Pandas Codebase?
The source code for Pandas is located at this github repository https://github.com/pandas-dev/pandas

```python
import pandas

mydataset = {
  'cars': ["BMW", "Volvo", "Ford"],
  'passings': [3, 7, 2]
}

myvar = pandas.DataFrame(mydataset)

print(myvar)
```
**checking pandas installed version:**
```
import pandas as pd

print(pd.__version__)
```
**Import pyplot from Matplotlib and visualize our DataFrame:**
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('data.csv')

df.plot()

plt.show()
```
**RESULT:**
![plot result](https://www.w3schools.com/python/pandas/img_pandas_plot.png)

