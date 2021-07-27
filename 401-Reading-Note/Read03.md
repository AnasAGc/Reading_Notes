## What is a file?

At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.

### File Paths

When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

* Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
* File Name: the actual name of the file
* Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

## Character Encodings

Another common problem that you may face is the encoding of the byte data. An encoding is a translation from byte data to human readable characters. This is typically done by assigning a numerical value to represent a character. The two most common encodings are the ASCII and UNICODE Formats. ASCII can only store 128 characters, while Unicode can contain up to 1,114,112 characters.

ASCII is actually a subset of Unicode (UTF-8), meaning that ASCII and Unicode share the same numerical to character values. It’s important to note that parsing a file with the incorrect character encoding can lead to failures or misrepresentation of the character. For example, if a file was created using the UTF-8 encoding, and you try to parse it using the ASCII encoding, if there is a character that is outside of those 128 values, then an error will be thrown.

## Opening and Closing a File in Python

When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object

``` file = open('dog_breeds.txt') ```

closing a file

* try-finally block:

```reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```

* with statement

```
with open('dog_breeds.txt') as reader:
```

# Python Exceptions

Raising an Exception:

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

## The try and except Block: Handling Exceptions

The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

### The else Clause

In Python, using the else statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.

``` try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    print('Executing the else clause.')
```
## Summary

![sda](https://files.realpython.com/media/try_except_else_finally.a7fac6c36c55.png)