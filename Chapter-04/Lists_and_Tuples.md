## Topics Covered
- [Lists in Python](#lists)
- [Features of Lists](#features-of-lists)
- [List Slicing](#list-slicing)
- List Methods
	- [sort()](#1-sort)
	- [reverse()](#2-reverse)
	- [append()](#3-append)
	- [extend()](#4-extend)
	- [insert()](#5-insert)
	- [pop()](#6-pop)
	- [remove()](#7-remove)
	- [index()](#8-index)
# Lists
-  Python list is a container to store a set of values of any data types.
					 OR
- A Python list is an ordered and mutable collection used to store multiple values of any data type.
### Features of Lists
- Ordered
- Mutable
- Allows duplicate values
- Can store different data types
### Example: 
```python
my_list = ["Hello", "World", 1, 5.1, True, ]

my_list[0] # return: "Hello"
```
>**NOTE:**
> List indexing is same as String.
# list slicing
- **List slicing** is a way to extract a portion (sub-list) from a list.
```python
my_list = [10, 20, 30, 40, 50]

print(my_list[1:4])
# Output: [20, 30, 40]
```

>**NOTE:**
>  Avoid using `list` as a variable name because `list()` is a built-in Python function.
# List Methods
## 1. sort()
- `sort()` method modifies the original list and arranges the elements in **ascending order**.
### Example: 
```python
my_list = [6,3,7,8,5,1]
my_list.sort()
print(my_list) # Output: [1, 3, 5, 6, 7, 8]
```
## 2. reverse()
- `reverse()` method reverses the order of elements in the list.
### Example: 
```python
my_list = [1,2,3,4,5,6]
my_list.reverse()
print(my_list) # Output: [6, 5, 4, 3, 2, 1]
```

## 3. append()
- `append()` method adds a single element to the end of the list.
### Example: 
```python
my_list = [1,2,3]
my_list.append(4)
print(my_list) # Output: [1, 2, 3, 4]

#------------------------------------------------- 

list1 = [1,2]
list1.append([3,4])
print(list1) # Output: [1, 2, [3, 4]]

# NOTE: Append adds the entire list, tuple, or set as a single element.
```

## 4. extend()
- `extend()` method use to Adds all elements from an iterable (list, tuple, set, string, etc.) to the end of the list.
	- **Iterable : ** An object capable of returning its members one at a time.
### Example: 
```python
my_list = [1,2]
my_list.extend([3,4])
print(my_list) # Output: [1, 2, 3, 4]

my_list.extend("AB") 
print(my_list) # Output: [1, 2, 3, 4, 'A', 'B']

# NOTE: extend() takes only one argument.
# my_list.extend(2,3) --> throw an error because here are two arguments
```

## 5. insert()
- `insert()` method used to inserts an element before the specified index.
### Example: 
```python
my_list = [1, 2, 3, 5]
# index:   0  1  2  3
my_list.insert(2,4) # insert(index, element)
print(my_list) # Output:[1, 2, 4, 3, 5] 
```

## 6. pop()
 - `pop()` method delete the element of a given index and return value.
 - Note: ** If no index is given it will delete the last element
### Example: 
```python
my_list = [1,2,3,4]
my_list.pop(2) # pop(index)
print(my_list) # Output:[1, 2, 4] 

#--------------------------------
list1 = [1,2,3,4]
c = list1.pop()
print(list1) # Output:[1, 2, 3] 
print(c) # Output: 4 (removed)
```

## 7. remove()
- `remove()` method deletes the first occurrence of a specified value from a list
### Example: 
```python
my_list = [1, 2, 3, 4, 5, 3]
my_list.remove(3)
print(my_list) # Output: [1, 2, 4, 5, 3]
```

## 8. index()
- `index()` method returns the index of the first occurrence of an element.
### Example: 
```python
my_list = [1, 2, 3, 4]
print(my_list.index(3)) # Output: 2
```

# Tuples in Python 
- A tuple is an ordered collection of elements of any data type.
### Features of Tuples
- Ordered
- Immutable
- Allows duplicate values
- Can store different data types
### Example: 
```python
# empty tuple
a = ()

# tuple with only one element
a = (1,)

# tuple with multiple element
a =(1,2,3,4,5)
```

>**NOTE:**
>- **Ordered** means elements stay in the same sequence you put them in.
>- **List = ordered + mutable**
>- **Tuple = ordered + immutable**

# Tuple methods
## 1. count()
- `count()` method tells the occurrence of an element.
### Example: 
```python
a = (1,2,3,4,2,5,2)
print(a.count(2)) # Output: 3
```
## 2. index()
- `index()` method in tuple tells the first occurrence of an element.
### Example: 
```python
a = (1,2,3,4,2,5,2)
print(a.index(2)) # Output: 1
```

