## Topics Covered

- [Variable](#variable)
- [Data Types](#data-types-in-python)
- [Rules for Defining a Variable Name](#rules-for-defining-a-variable-name)
- [Operators in Python](#operators-in-python)
- [Truth Table](#truth-table)
- [Floor Division](#floor-division)
- [Type() Function](#type-function)
- [Typecasting](#typecasting)
- [Input() Function](#input-function)
---
# Variable
A variable is the name given to a memory location in a program.
						OR
A variable is a container which stores values.

# Data types in python

|  No.  |       Data Type       |  Keyword  |   Example    |         Notes          |
| :---: | :-------------------: | :-------: | :----------: | :--------------------: |
| **1** |        Integer        |  **int**  |      5       |      Whole number      |
| **2** | Floating Point Number | **float** |     5.0      |     Decimal number     |
| **3** |        String         |  **str**  |   "Hello"    | Text(always in quotes) |
| **4** |        Boolean        | **bool**  | True / False |     True or False      |
| **5** |       NoneType        |   None    |     None     |   Represent no value   |

>**Notes:**
>- Python automatically identifies the data type of a value.
>- **Keyword :** reserve word in python.
>- **Identifiers :** class/function/ variable name

```python
a = 5 # identify a as <class 'int'>
b = 9.5 # identify b as <class 'float'>
name = "Shlok" # identify name as <class 'str'>
```

# Rules for defining a variable name
- A variable name can contain alphabets, digits, and underscores. 
- A variable name can only start with an alphabet or an underscore( _ ).
- A variable name can’t start with a digit.
- No white space is allowed to be used inside a variable name.
- Examples : shlok, shl8k, `_shlok`

# Operators in python
An operator is a symbol used to perform a specific operation on variables.
1. **Arithmetic Operators :** +, -, * , / 
2. **Assignment Operators :** =, +=, -=
3. **Comparison Operators :**` ==`, >, >=, <, <=, !=
4. **Logical Operators :** and, or, not

```python
# Arithmetic Operators: 

print(5+7) # Output: 12
# Here
# 5 & 7 --> operands
# + --> operator 
# 12 --> result 
# ------------------------------------------------------
# Assignment Operators:
 
 a = 7 # assign value 7 in variable a
 a += 3 # increment value of a by 3 (Output: 10)
 
 b = 10
 b -= 5 # decrement value of a by 5 (Output: 5)
 print(a==b) # == (double equal to) used to compare to variable
 # ------------------------------------------------------
 # Comparison Operators: 
 
 a = 5==5 # Output: True
 b = 6>=7 # Output: False
```

>**Note**
>- `=` used to assign value in a variable
>- `==` used to compare two variable

# Truth Table

## Truth table of 'and'
- Result is true only if both condition are true
```python
print(True and True) # Output : True
print(True and False) # Output : False
print(False and True) # Output : False
print(False and False) # Output : False
```
##  Truth table of 'or'
- Result is true if at least of the condition is true
```python
print(True or True) # Output : True
print(True or False) # Output : True
print(False or True) # Output : True
print(False or False) # Output : False
```
## Truth table of 'not'
- Result is true if condition is false and false if condition is true
```python
print(not True) # Output : False
print(not False) # Output : True
```
### Floor Division
1. If number is positive then python ignore the decimal values.
2. If the result is negative, Python rounds down to the nearest smaller integer. 

```python
5 // 3       # Output: 1    (5/3 = 1.66)
-5 // 3      # Output: -2   (-5/3 = -1.66)
5.0 // 3.0   # Output: 1.0   (5.0/3.0 = 1.66)
-5.0 // 3.0  # Output: -2.0   (-5.0/3.0 = -1.66)
```

# Type() Function
type() function used to find the data type of a given variable in python.
```python
a = 5;
print(type(a)) # output : <class 'int'>
```

# Typecasting
One data type can be converted in to another data type. 
```python
a = int("5") # String to int
b = float(a) # int to float
c = str(a) # int to string
```

# Input() Function
- Take input from user.
```python
a = input("Enter a number: ") # take String input & store it in variable A
b = int(input("Enter a number: ")) # take integer input
```

>**Note:**
Python take input as a string by default.

