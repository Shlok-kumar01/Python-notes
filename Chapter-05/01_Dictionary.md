## Topics Covered

- [Dictionary](#dictionary)
- [Properties of Dictionary](#properties-of-dictionary)
- [Dictionary Methods](#dictionary-methods)
  - [items()](#1-items)
  - [keys()](#2-keys)
  - [update()](#3-update)
  - [pop()](#4-pop)
  - [get()](#5-get)
  - [values()](#6-values)
- [dict[key] vs dict.get(key)](#dictkey-vs-dictgetkey)
---
# Dictionary
- A dictionary is a collection of key-value pairs.
## Properties of dictionary
- Unordered (Element’s order doesn’t matter)
- mutable
- **Key-indexed** ( elements are accessed using keys, not numeric indexes)
- Values can be duplicated
## Syntax:
```python
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

print(a["Name"]) # Output: Shlok
print(a["Marks"]) # Output: 100
```

>**NOTE:**  
>  Keys must be unique.

## What if I create duplicate keys
- Python does not raise an error.
- If same key appear multiple times the last value overwrite the previous value.
```python
student = {
	"name" : "Shlok",
	"age" : 20,
	"name" : "Rahul"
}

print(student)
# Output: {'name': 'Rahul', 'age': 20}
```

---
# Dictionary Methods
- Some commonly used dictionary methods are:
## 1. items()
- `items()` method returns all key-value pairs as tuples.
### Example: 
```python 
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

b = a.items()
print(b)
# Output: dict_items([('key', 'value'), ('Name', 'Shlok'), ('Subject', 'Python'), ('Marks', 100)])
```

## 2. keys()
- `keys()` method returns all keys of the dictionary.
### Example: 
```python
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

b = a.keys()
print(b)
# Output: dict_keys(['key', 'Name', 'Subject', 'Marks'])
```

## 3. update()
- The `update()` method updates a dictionary by adding new key-value pairs or modifying existing ones.
- **Note: ** It modifies the original dictionary and returns None.
### Example:
```python
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

a.update({"Name" : "Rahul"})
print(a) 
# Output: {'key': 'value', 'Name': 'Rahul', 'Subject': 'Python', 'Marks': 100}

b = a.update({"Name" : "Rahul"})
print(b) # Output: None (Update method return None)
```

## 4. pop()
- `pop()` method removes the specified key and returns its value.

### Example: 
```python
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

b = a.pop("Name")

print(b) # Output: Shlok

print(a) 
# Output: {'key': 'value', 'Subject': 'Python', 'Marks': 100}
```
## 5. get()
- `get()` method returns the value of the specified keys.
## Example:
```python
a = {
	"key" : "value",
	"Name" : "Shlok",
	"Subject" : "Python",
	"Marks" : 100,
}

b = a.get("Name") 
print(b) # Output: Shlok
```

## 6. values()
- Returns all values in the dictionary.
## Example:
```python
a = {
    "Name": "Shlok",
    "Marks": 100
}

print(a.values()) 
# Output: dict_values(['Shlok', 100])
```
---
# dict[key] vs dict.get(key)
- `dict[key]` raises a `KeyError` if the key is not found, while `dict.get(key)` returns `None` 
## Example:
```python
a = {
	"key" : "value",
	"Name" : "Aarush",
	"Subject" : "Python",
	"Marks" : 100,
}

b = a.get("Date")
print(b) # Output: None

print(a["Date"]) # Output: error 
```
