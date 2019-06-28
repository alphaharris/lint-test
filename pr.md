# How to record the cumulative sum of a list in Python

While summing over a list, one may wish to record intermediate sums as the list is processed from left to right.

## Use `numpy.cumsum()`

```python
#PRELUDE
import numpy as np 

#CODE
x = [1,2,3]
y = list(np.cumsum(x))

#OUTPUT
print(y)
#output: [1,3,6]
```
`cumsum()` calculates the desired cumulative sum. `list()` casts the numpy array into a Python list.

## Use `itertools.accumulate()`

```python
#PRELUDE
import itertools

#CODE
x = [1,2,3]
y = list(itertools.accumulate(x))

#OUTPUT:
print(y)
#output: [1,3,6]
```
`itertools()` also calculates the desired cumulative sum. It is less readable but more efficient than `np.cumsum()`.
