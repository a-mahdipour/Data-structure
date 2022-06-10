# Data-structure (Python-based)

*There are several data sctructures in Python, similar to other programming languages such as R, Java, C++ and so on.  In here, we briefly go through them and investigate their similarities and differences as Python objects. We mayn also see their association/dissimilarities with similar data stuctures in other programming languages.*
-----
## 1. Lists (arrays)
In general, arrays are contiguous data structures of homogeneous elements (of the same data type) which are located in adjacent chunks of memory with specific assigned indexes (elements are ordered) that can be easily manipulated. Arrays, however, are not built-in data structures in python and need to be declared via either **Array** or **NumPy** modules. Arrays acquire constant size that remain unchanged. Arrays are mutable data structures and are usually suitable for large data.

```
## Using array module
import array
array1 = array.array(['a','ab','c','d'])

## Using NumPy to generate a numpy array:
import numpy as np
array2 = np.array(['a','ab','c','d'])
```
In Python, a list is an ordered collection of objects that can have different types (lists are nested: can contain heterogeneous elements). The order in lists provides unique indexes for each element which remains unchanged. Lists and arrays are both mutable and in contrast with that of in Java, Python's lists are not static and can be automatically scaled up/down. Lists are more suitable to store small amount of data and cannot be used directly by many operations. Some operations to be used for lists are listed in bellow. 

```
## defining a list
list1 = ['abc', 3.56, -10, 2*pi]

## add an object
list1.append("new")

## delete the first item
list1.pop(1)

## permute i-th and j-th items
a=list1[i-1]
b=list1[j-1]
list1[i-1], list[j-1] = b,a

## defining an array as an special case of lists:
array = [-2,45,12,-7,0,31]

## move elements
[*list1, list1.pop(0)]
print(list1)
```
-----
## 2. Queue
Queues are linear data structures that work based on first-in-first-out order in which items are not accessible via their indexes. In a queue we only can pull out the oldest item added which makes this objects very useful for those tasks that are desinged based on the porder of attendence (e.g. lines in grocery shops). ```append()``` and ```pop()``` are used to resp. add and remove the newest and oldest elements to the queue. Using Python's collection module, provides the possibility of accesss to both sides of the queue (a double-ended queue) using ```popleft()``` and ```popright()```.

```
from collections import deque
## defining a queue
qu = deque()
 
## Adding elements to a queue
qu.append('element1')
qu.append('element2')
qu.append('element3')
print("Updated queue:")
print(qu)

## Deleting elements 
print(qu.popleft())
print(qu.popright())
```

-----
## 3. Tuples 
