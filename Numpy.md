# Numpy
NumPy(Numerical Python) is a opensource python library used for working with arrays.created in 2005 by **Travis Oliphant** 

# Numpy vs List
NumPy is fast because
it uses fixed type, contiguous memory & is smaller in size

# Basics

pip install numpy
```python
import numpy as np

a = np.array([[1,2],[3,4]], dtype='int32')

a.size
a.shape
a.itemsize
```
## Initialization
``` python
# All 0s
np.zeros((2,3))

# All 1s
np.ones((2,3))

# Any other number example  a 2x3 matrix of 5s
np.full((2,3),5)

# full_like -> generates an array of shape a having all 5s
np.full_like(a, 5)

#random numbers
np.random.rand(4,2)
np.random.random_sample((4,2))
np.random.randint(7, size=(3,2))
np.random.randint(7, 10, size=(3,2))

#Identity
np.identity (5)

#Repeat
arr = np.array([[1,2,3]])
np.repeat(arr, 3)

#Copying (Be aware!!!)
b=a # points to same array
b=a.copy() # makes a copy

```

## Mathematics

```python
# elmentwise arithmatic
a = np.array([1,2,3,4])
a+2 # => [-1,0,1,2]
a-2 # => [1,2,3,4]
. 
.
.

np.sin(a)
np.cos(a)
```

## Linear Algebra

```python
# matrix multiplication
 np.matmul(a,b)
 
# find determinant
np.linalg.det(a) 

# eigen values

# trace 

# inverse

```

## Statistics
```python

np.min(a, axis=1) # Axis=1 gives column array of min numbers 

 
```

## Reorganizing Arrays
```python
a = b.reshape((8,1))

# vertical stacking

np.vstack((a,b,a,b,b))
np.hstack((a,b,a,b,b))

```

## Miscellaneous

```python

# From file
filedata = np.genfromtxt('data.txt', delimiter=',').astype('int32')

# Boolean Masking Advanced indexing

filedata > 50
a = filedata[ filedata > 50]

# List Indexing
a = np.array([1,2,3,4,5,6,7,8,9])
a[[1,2,8]] => [2,3,9]


 
```



