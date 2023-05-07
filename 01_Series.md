# Series

[**Series**](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#series): is a one-dimensional labeled array capable of holding any data type (integers, strings, floating point numbers, Python objects, etc.). The axis labels are collectively referred to as the index. The basic method to create a Series is to call:
  ````
  >>> s = pd.Series(data, index=index)
  ````

  Here, data can be many different things:

  - a Python dict

  - an ndarray

  - a scalar value (like 5)
