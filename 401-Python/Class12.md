# Pandas

```In [1]: import numpy as np```

```In [2]: import pandas as pd```

### Object Creation

Creating a series: ```In [3]: s = pd.Series([1, 3, 5, np.nan, 6, 8])```
Creating a DataFrame with Numpy Array: ```xIn [5]: dates = pd.date_range('20130101', periods=6)```
Creating a DataFrame with Dict of objects: 
```
df2 = pd.DataFrame({
    'A': 1.,
    'B': pd.Timestamp('20130102'),
    'C': pd.Series(1, index=list(range(4)), dtype='float32'),
    'D': np.array([3] * 4, dtype='int32'),
    'E': pd.Categorical(["test", "train", "test", "train"]),
    'F': 'foo'})
```
**DataFrame.to_numpy()** gives a NumPy representation of the underlying data. Note that this can be an expensive operation when your *DataFrame* has columns with different data types, which comes down to a fundamental difference between pandas and NumPy: NumPy arrays have one dtype for the entire array, while pandas DataFrames have one dtype per column. When you call **DataFrame.to_numpy()**, pandas will find the NumPy dtype that can hold all of the dtypes in the *DataFrame*. This may end up being object, which requires casting every value to a Python object.

>describe( ) shows a quick statistic summary of your data:

