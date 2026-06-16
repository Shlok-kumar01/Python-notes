## Topics Covered

- [String](#string)
- [String Indexing](#index-value)
- [Negative Indices](#negative-indices)
- [String Slicing](#string-slicing)
- [Slicing with Skip Value](#slicing-with-skip-value)
- [String Functions](#string-functions)
- [Escape Sequence Characters](#escape-sequence-character)
---
# String
String is a sequence of characters enclosed in quotes.
```python
a = 'shlok' # single quoted string.
b = "shlok" # double quoted string.
c = '''shlok''' # triple quoted string.
```
## Index value 
- $S\rightarrow0$ 
- $h \rightarrow1$
- $l\rightarrow 2$
- $o\rightarrow3$
- $k\rightarrow4$
>String index start from 0 to (length-1)

## Negative indices

- $S\rightarrow-5$ 
- $h \rightarrow-4$
- $l\rightarrow-3$
- $o\rightarrow-2$
- $k\rightarrow-1$ 
---
# String Slicing
In python we slice a string to get a part of the string.
- slice = name(first index : last index)
- Here, First index included & last index excluded

```python
a = "Shlok"
b = a[0:2] # Return: Sh (last index excuded)
c = a[:2] # goes from 0 to given index

d = a[0:4] # Return: Shlo
e = a[0:] # Return: shlok (goes from 0 to last index)
f = a[:] # Return: shlok (goes from 0 to last index)

f = a[-5:-1] # Return: Shlo
f = a[0:4] # corresponding positive index
# convert the negetive index into corresponding positive index for better understanding
```

# Slicing with skip value 
- We can also provide a skip value while slicing a string.
## Syntax
```python
# a = name[start : stop : step]

# step = 1 --> normal
# step = 2 --> skip 1
# step = 3 --> skip 2
# step = n --> skip (n-1)
# step = -1 --> reverse
```

## Example 
```python
a = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
print(a[0:8:2]) # Output:ACEG (index 0[A] : index 8[I] : skip 1 Character) 
# 'A' b 'C' d 'E' f 'G' h 'I' ---> ACEG (last index excluded)

print(a[3:18:7]) # Output : DKR
print(a[::-1]) # reverse the string
```

# String functions
- String functions are built in functions used to perform operations and manipulate strings.

## 1. len()
- Returns the lengths of the string
```python
str = "shlok"
print(len(str)) # Output: 5
```

## 2. str.startswith(" ")
- Checks if string starts with a value.
```python
text = "shlok"
print(text.startswith("sh")) # Output: True
```
## 3. str.endswith(" ")
- Check whether string ends with the specified value or not.
```python
str = "shlok"
print(str.endswith("ok")) # Output: True
```

## 4. str.count(" ")
- Count occurrences (return numbers of time a specific value appear)
```python
str = "shloook"
print(str.count("o")) # output: 3 
```

## 5. str.capitalize()
- It makes the first letter of the string capital
```python
str = "shlok"
print(str.capitalize()) # Output: "Shlok"
```

## 6. str.find(" ")
- Return the index of the first occurrence of a specified value in a string.
```python
str = "shlook"
print(str.find("oo")) # Output: 3
```

## 7. str.replace()
- This function replace old word with new word in the entire string
```python
str = "shlokkk"
print(str.replace("k","w")) # Output: "shlowww"
```

## 8. str.lower()
- Converts all characters to lowercase
```python
str = "SHLOK"
print(str.lower()) # Output: "shlok"
```


## 9. str.upper()
Converts all characters to uppercase.
```python
text = "shlok"
print(text.upper()) # Output: "SHLOK"
```

## 10. str.strip()
Removes spaces from start and end.
```python
text = "  shlok  "
print(text.strip()) # Output: "shlok"
```

---
# Escape sequence character
-  Escape sequences are special characters that begin with a backslash ( \ ).
# Escape Sequence Characters in Python

| Escape Sequence | Meaning         | Example          | Output          |
| --------------- | --------------- | ---------------- | --------------- |
| `\n`            | New line        | `"Hello\nWorld"` | Hello<br>World  |
| `\t`            | Tab space       | `"Hello\tWorld"` | Hello  World    |
| `\\`            | Backslash       | `"Hello\\World"` | Hello\World     |
| `\'`            | Single quote    | `'It\'s OK'`     | It's OK         |
| `\"`            | Double quote    | `"\"Hello\""`    | "Hello"         |
| `\r`            | Carriage return | `"Hello\rHi"`    | Hi (overwrites) |
| `\b`            | Backspace       | `"Helloo\b"`     | Hello           |


>**Note:**
>Strings are immutable, which means their value cannot be changed after they are created.

