# Covered Topics

- [Introduction](#introduction)
  - [Memory Types](#introduction)
  - [Files](#files)
  - [Types of Files](#types-of-files)
    - [Text Files](#text-files)
    - [Binary Files](#binary-files)

- [File Operations in Python](#file-operations-in-python)
  - [Opening a File](#opening-a-file)
  - [Reading Files](#reading-files)
    - [read()](#1-read)
    - [readline()](#2-readline)
    - [readlines()](#3-readlines)
  - [Writing Files](#writing-files)
  - [Appending Data](#appending-data)
  - [Closing Files](#closing-files)
  - [With Statement](#with-statement)

  
---
# Introduction
- Computers store data in two types of memory.

| Memory Type         | Description                                                 | Example             |
| ------------------- | ----------------------------------------------------------- | ------------------- |
| Volatile Memory     | Data is lost when the program stops or power is turned off. | RAM                 |
| Non-Volatile Memory | Data remains stored permanently.                            | HDD, SSD, Pen Drive |
---
## Files
- A file is a collection of data stored on a storage device.
- Variables and RAM store data temporarily. Once a program ends, the data disappears
- Python can read from files and write to files.
### Types of files
- Python mainly works with two types of files:
#### Text Files
- Human-readable files.
- Examples: `.txt`, `.py` `.c` etc.
#### Binary Files
- Stored in binary format(0s and 1s).
- Cannot be read directly by humans.
- Examples: `.jpg`, `.mp4`, `mp3`, `.dat`
---
# File Operations in Python
- The four basic file operations are:
1. Open a file
2. Read a file
3. Write to a file
4. Close a file

```text
Open → Read/Write → Close
```

## Opening a File
- Python provides the `open()` function to open a file.
### Syntax:
```python
open("filename", "mode") 
```

### Example:
```python
# Open file for read
f = open("file.txt", "r")

# Read its content
text = f.read()

# Print its content
print(text)

# Close the file
f.close()
```

>**NOTE:**
>- If the file is not in the current working directory, Python will raise a `FileNotFoundError`.
>- To access files in other folders, use a relative or absolute file path.

## File Modes
|Mode|Description|
|---|---|
|`"r"`|Read file|
|`"w"`|Write file (creates new file or overwrites existing content)|
|`"a"`|Append data to file|
|`"x"`|Create a new file|
|`"r+"`|Read and write|
|`"rb"`|Read binary file|
|`"wb"`|Write binary file|
## Reading Files

### 1. read()
- Read entire file.
#### Example:
```python
# Open the file
file = open("note.txt", "r")

# read its content
content = file.read()

# print the content
print(content)

# close the file
file.close()
```

### 2. readline()
- Reads one line at a time.
#### Example:
```python
file = open("notes.txt", "r")

print(file.readline()) # Print first line
print(file.readline()) # Print second line

file.close()
```

### 3. readlines()
- Returns all lines as a list.
#### Example:
```python
file = open("notes.txt", "r")

lines = file.readlines()

print(lines)

file.close()
```
---
## Writing Files
### write()
- `w` mode used to write
#### Example:
```python
file = open("notes.txt", "w")

file.write("Hello Python")

file.close()
```

>**NOTE:**  
>`w` mode deletes old content before writing.

## Appending Data
- `a` mode appends data to the end of a file.
### Example: 
```python
file = open("notes.txt", "a")

file.write("\nHello") # append Hello

file.close()
```

## Closing Files
- Always close files after use.
- This helps to:
	- Saves changes
	- Frees system resources
	- Prevents file corruption
### Syntax:
```python
file.close()
```

## With Statement
- The best way to open and close a file automatically is by using the `with` statement.
- Python automatically closes the file when the `with` block ends.
### Example:
```python
with open("notes.txt", "r") as file:
    content = file.read() 
       
    print(content) 
```
