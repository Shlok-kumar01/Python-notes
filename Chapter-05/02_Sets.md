## Topics Covered

- [Sets in Python](#set)
- [Properties of Set](#properties-of-set)
- [Dictionary vs Set](#dictionary-vs-set)
- [Operations on Set](#operations-on-set)
  - [len()](#1-len)
  - [remove()](#2-remove)
  - [pop()](#3-pop)
  - [clear()](#4-clear)
  - [union()](#5-union)
  - [intersection()](#6-intersection)
  - [difference()](#7-difference)
---
# Set
- Set is a collection of non-repetitive elements.
## Properties of set
-  Stores only unique values (duplicates are automatically removed)
- Unordered (Elements do not have a fixed position and may appear in different order each time)
- Unindexed (cannot access elements using index)
- Mutable (you can add/remove elements)
## Example:
```python
#---------------- EMPTY SET --------------------
a = set() # Empty set 
a.add(1)
a.add(2)
print(a) # Output: {1, 2}

# --------------- SET WITH ELEMENTS ------------
b = {1, 2, 2, 3, "hello", 1.5} # set remove duplicate elements
print(b) # Output: {1, 2, 3, 1.5, 'hello'} 

#---------------- UNORDERED --------------------
a = {5, 6, 8, 4, 7, 3}
print(a) 
# Output: {3, 4, 5, 6, 7, 8}

#---------------- UNINDEXED --------------------
a = {5, 6, 8, 4, 7, 3}
print(a[4]) # Output: error

#---------------- MUTABLE ----------------------
a = {5, 6, 8, 4, 7, 3}
a.remove(8)
print(a) # Output: {3, 4, 5, 6, 7}
```


> **NOTE:**  
> Empty set is declared using `set()` because `{}` creates an empty dictionary.

# Dictionary vs set
- Both dictionary and set use curly braces `{}` in Python.  
- The main difference is that dictionaries store **key-value pairs**, while sets store only **unique values**.
```python
#----------DICTONARY -------------
a = { # key value pairs
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}
#----------- SET ----------------
b = {9, 7, 8.5, "shlok", 100}

#--------------------------------
# empty dictionary
a = {} 

# empty set
a = set() 
```
---

# Operations on set
## 1. len()
- `len()` return the length of the set.

### Example: 
```python
a = {7,5,3,4,9,2}
print(len(a)) # Output: 6
```

## 2. remove()
-  `remove()` deletes the specified element from the set.
### Example: 
```python
a = {7,5,3,4,9,2}
a.remove(3)
print(a) # Output: {2, 4, 5, 7, 9}
```

## 3. pop()
- `pop()` remove an arbitrary element(random) from set and return the removed element
### Example: 
```python
a = {7,5,3,4,9,2}
b = a.pop()
print(b) # Output: suppose it remove element 2
print(a) # Output: {7, 5, 3, 4, 9}
```


## 4. clear()
- `clear()` empty the set.
### Example: 
```python
a = {7,5,3,4,9,2}
a.clear()
print(a) # Output: set()
```

## 5. union()
- `union()` returns a new set containing all unique elements from both sets..
### Example: 
```python
a = {1,2,3,4,3,5,4}
b = {6,7,3,6,4,8,9,2}

c = a.union(b)
print(c) # Output: {1, 2, 3, 4, 5, 6, 7, 8, 9}
```

## 6. intersection()
- `intersection()` return a set which contains only item in both sets.
### Example: 
```python
a = {1,2,3,4,3,5,4}
b = {6,7,3,6,4,8,9,2}

c = a.intersection(b)
print(c) # Output: {2, 3, 4}
```

## 7. difference()
- `difference()` return the unique elements which is not available in other set.
### Example: 
```python
a = {1,2,3,4,3,5,4}
b = {6,7,3,6,4,8,9,2}

c = a.difference(b)
print(c) # Output: {1, 5}
```

