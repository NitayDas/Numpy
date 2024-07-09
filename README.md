# NumPy Basics Project

Welcome to the NumPy Basics Project! This project is designed to help you get started with NumPy, a powerful numerical computing library in Python.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Basic Usage](#basic-usage)
  - [Creating Arrays](#creating-arrays)
  - [Array Operations](#array-operations)
  - [Indexing and Slicing](#indexing-and-slicing)
  - [Common Functions](#common-functions)
- [Contributing](#contributing)
- [License](#license)

## Introduction

NumPy refers numerical python is the fundamental package for scientific computing in Python. It provides support for arrays, matrices, and many mathematical functions.

## Installation

To install NumPy, you need to have Python installed on your system. You can install NumPy using pip:

```bash
pip install numpy
```

Alternatively, if you are using Anaconda, you can install NumPy using conda:

```bash

conda install numpy
```

## Basic Usage

Here are some basic examples to get you started with NumPy.

## Creating Arrays

You can create NumPy arrays using the numpy.array function:

```python
import numpy as np

# Create a 1D array
array_1d = np.array([1, 2, 3, 4, 5])
print(array_1d)

# Create a 2D array
array_2d = np.array([[1, 2, 3], [4, 5, 6]])
print(array_2d)

# creating a array using arrange

arr = np.arrange(10)
print(arr)

[0,1,2,3,4,5,6,7,8,9]

#bool array

arr = np.ones(5,dtype=bool)
print(arr)

[ True  True  True  True  True]

#one_Array

import numpy as np
oneArray = np.ones([4,3])
oneArray

array([[1., 1., 1.],
       [1., 1., 1.],
       [1., 1., 1.],
       [1., 1., 1.]])

# Eye array

import numpy as np
EyeArray = np.eye(3)
EyeArray

array([[1., 0., 0.],
       [0., 1., 0.],
       [0., 0., 1.]])

#set_diagonal element using diag function

import numpy as np
arr2= np.diag([3,6,7])
print(arr2)
print("\n")
print(np.diag(arr2))

[[3 0 0]
 [0 6 0]
 [0 0 7]]

[3 6 7]

#random number generate with max,min,and total values

import numpy as np
arr = np.random.randint(3,9,6)
arr
array([3, 8, 4, 6, 5, 8])

#random number generate between 0 and 1

import numpy as np
random_array = np.random.rand(2,3)
print(random_array)

array([[0.4543757 , 0.89930504, 0.38307286],
       [0.9099233 , 0.9006465 , 0.00388887]])


```

## Array Operations

NumPy allows you to perform element-wise operations on arrays:

```python

# Element-wise addition
array_sum = array + 2
print(array_sum)

# Element-wise multiplication
array_product = array * 2
print(array_product)

#extract items that satisfy a given condition from 1D array.

# using where gives the position of the array elements
import numpy as np
arr = np.array([1,2,3,8,8,9,5,2,4,6,4])
element_is_four = np.where(arr==4)
rem_zero = np.where((arr%3) == 0)

#this method gives the element itself
rem_one = arr[arr%3==0]

print(rem_zero)
print()
print(rem_one)
print()
print(ans)

(array([2, 5, 9], dtype=int64),)
[3 9 6]
(array([ 8, 10], dtype=int64),)


#sorting

import numpy as np
arr = np.array([1,8,3,8,2,9,5,2,4,6,4])
arr2 = np.array(['a','v','m','l','k'])

print(np.sort(arr))
print()
print(np.sort(arr2))

[1 2 2 3 4 4 5 6 8 8 9]
['a' 'k' 'l' 'm' 'v']

#searchsorted
#it gives the count of the elemnt that are less than the given element

import numpy as np
arr = np.array([1,2,3,4,4,6,7,7,8,9])

ans = np.searchsorted(arr, 5)
group = np.searchsorted(arr, [5,2,7])

print(ans)
print()
print(group)

5
[5 1 6]

​
#Filter using a bool array

import numpy as np​
arr = np.array(['a','v','m','l','k'])
f=[True,False,True,True,False]

filtered_array = arr[f]
print(filtered_array)

#filtered element where f has True value
['a' 'm' 'l']

#for unique element

import numpy as np
arr = np.array([1,2,3,8,8,9,5,2,4,6,4])
unique_array= np.unique(arr)

print(unique_array)

[1 2 3 4 5 6 8 9]

# for Resize an array

import numpy as np
arr = np.array([1,2,3,8,8,9,5,2,4,6,4,3])
resize_array = np.resize(arr,(3,4))

print(resize_array)

[[1 2 3 8]
 [8 9 5 2]
 [4 6 4 3]]







```

## Indexing and Slicing

You can access elements of a NumPy array using indexing and slicing:

```python

# Indexing
first_element = array_1d[0]
print(first_element)

# Slicing
subset_array = array_1d[1:4]
print(subset_array)
```

## Common Functions

NumPy provides many useful functions for mathematical operations:

```python

# Mean of an array
mean_value = np.mean(array_1d)
print(mean_value)

# Standard deviation of an array
std_deviation = np.std(array_1d)
print(std_deviation)

# Sum of all elements in an array
sum_of_elements = np.sum(array_1d)
print(sum_of_elements)
```



