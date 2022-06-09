# Data-structure (Python-based)

*There are several data sctructures in Python, similar to other programming languages, and we briefly go through them in bellow.
Lists, sets and tuples are the basic strutures in Python and more complicated structures are dictionaries, maps, hash tables, trees and graphs*
-----
## 1. Lists (arrays)

In Python, a list is an ordered collection of objects that can have different types (lists are nested). The order in lists provides unique indexes for each element which remains unchanged. lists/arrays are mutable. There exists no built-in array in Python and are basically those lists that have homogenous elements of the same type. In contrast with Java, Python's lists/arrays are not static and can be automatically scaled up/down.

add, shift, move, and delete elements

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
