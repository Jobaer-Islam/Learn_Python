
# Python Basics – Print Function

## Introduction

* In Python, you can output text, numbers, or other values using the **`print()` function**.
* Unlike some languages (C → `printf`, C++ → `cout`, Java → `System.out.print`), Python has a simple built-in function: **`print()`**.
* You do **not** need to import libraries or write a `main()` function just to print something.

---

## Printing Text

* Example:

  ```python
  print("Hello World")
  ```
* Output:

  ```
  Hello World
  ```
* Printing requires just **one line of code**.

---

## Printing Different Data Types

* You can print **strings, numbers, booleans**, etc.
* Examples:

  ```python
  print("Hello")      # String
  print(123)          # Integer
  print(3.14)         # Float
  print(True, False)  # Booleans
  ```

---

## Printing Multiple Items

* You can print **multiple values together** in a single statement by separating them with commas.
* Example:

  ```python
  print("Bangladesh", "Pakistan", "Afganistan", "Palestine")
  ```
* Output:

  ```
  Bangladesh Pakistan Afganistan Palestine
  ```
* You can also mix data types:

  ```python
  print("Bangladesh", True, 2025)
  ```

---

## `sep` Parameter (Separator)

* By default, multiple values are separated by a **space**.
* You can change this using the `sep` parameter.
* Example:

  ```python
  print("Apple", "Banana", "Cherry", sep=", ")
  ```
* Output:

  ```
  Apple, Banana, Cherry
  ```

---

## `end` Parameter

* By default, every `print()` ends with a **newline** (`\n`).
* You can change this with the `end` parameter.
* Example:

  ```python
  print("Hello", end=" ")
  print("World")
  ```
* Output:

  ```
  Hello World
  ```

---

## Documentation

* In environments like **Anaconda/Jupyter**, you can check documentation with `help(print)` or `print?`.
* This shows that:

  * `print` accepts multiple values.
  * It has optional parameters like `sep`, `end`, and `file`.

---

## Why `print` is Important

* **Flexible**: works with any number of arguments.
* **Powerful**: can control spacing (`sep`) and line breaks (`end`).
* **Frequently used**: even in large projects, you’ll rely on `print()` for debugging and displaying output.
* Advanced parameters (`file`, `flush`) are mostly used in file handling or logging (covered later).

---


# Python Data Types 

## Main Categories

* Python data types can be divided into **three categories**:

  1. **Basic Types**
  2. **Container Types**
  3. **User-Defined Types**

---

## 1. Basic Types

* **Integer (`int`)**

  * Whole numbers (positive or negative).
  * Example: `x = 10`
  * Python allows very **large integers** with no fixed limit (unlike many other languages).
  * Example:

    ```python
    x = 10**309
    print(x)
    ```

    Python can still handle this, though it may display `infinity` beyond certain ranges.

* **Float (`float`)**

  * Decimal numbers.
  * Example: `y = 3.14`
  * Supports very large floating-point numbers.
  * For most practical purposes, floats behave like large decimals but may show `inf` (infinity) if too large.

* **Boolean (`bool`)**

  * Two possible values: `True` or `False`.
  * Widely used in conditions and logical operations.

* **Complex (`complex`)**

  * Represents complex numbers (mathematics).
  * Example: `z = 3 + 4j`
  * Mostly useful in mathematical or scientific applications.

* **String (`str`)**

  * Sequence of characters.
  * Example:

    ```python
    s1 = 'Hello'
    s2 = "World"
    s3 = '''This is 
    a multiline string'''
    ```
  * Can be defined with single (`'`), double (`"`), or triple (`'''` / `"""`) quotes.
  * Strings are very commonly used in applications.

---

## 2. Container Types

* Used to store multiple values in one variable.

### List

* Ordered, mutable (can be changed).
* Example:

  ```python
  fruits = ["apple", "banana", "cherry"]
  ```
* Uses **square brackets `[]`**.

### Tuple

* Ordered, immutable (cannot be changed).
* Example:

  ```python
  numbers = (1, 2, 3)
  ```
* Uses **round brackets `()`**.

### Set

* Unordered collection of unique elements.
* Example:

  ```python
  myset = {1, 2, 3, 4}
  ```
* Supports set operations (union, intersection, etc.).

### Dictionary (`dict`)

* Stores **key–value pairs**.
* Example:

  ```python
  person = {"name": "Jobaer", "age": 25, "gender": "Male"}
  ```
* Keys must be unique; values can be any data type.

---

## 3. User-Defined Types

* Created by the programmer using **classes and objects**.
* Example (to be learned in Object-Oriented Programming):

  ```python
  class Student:
      def __init__(self, name, roll):
          self.name = name
          self.roll = roll
  ```

---

## Summary

* **Basic Types** → int, float, bool, complex, str.
* **Container Types** → list, tuple, set, dict.
* **User-Defined Types** → classes & objects (covered later in OOP).

---

# Python Comments

## What are Comments?

* **Definition**: Comments are parts of code that are **not executable** by the compiler or interpreter.
* They are ignored completely during execution.
* Example:

  ```python
  # This is a comment
  print("Hello")
  ```

  Output → `Hello` (comment ignored)

---

## Why Use Comments?

1. **Teamwork**

   * In companies, code is written in teams.
   * If you leave, take leave, or someone else takes over your code, comments help them understand the logic.
   * Without comments, the company may face problems if the code is unclear.

2. **For Yourself**

   * After months, even you may forget what logic you used.
   * Comments act as **documentation** for your own reference.

3. **Overall Benefit**

   * Comments **improve code readability**.
   * They benefit your teammates immediately and benefit you in the long run.

---

## Writing Comments in Python

* Python supports comments using the **hash `#` symbol**.
* Anything after `#` on the same line is ignored.

**Examples**

```python
# This prints Hello World
print("Hello World")

# This is another comment
print(42)
```

---

## Multi-line Comments

* Python does **not** have a true multi-line comment feature.
* To write multiple lines, you must start each line with `#`.

**Example**

```python
# Line 1
# Line 2
# Line 3
```

* Some IDEs provide a shortcut to toggle multiple lines as comments, but at the language level, Python only has single-line `#` comments.

**Note:** This is not a big limitation. Usually, comments are 1–3 lines, not long paragraphs.

---

## Practical Advice

* Comments are not about writing essays. Keep them **short, clear, and helpful**.
* Six years of coding experience (as per transcript) → never found lack of multi-line comments a real problem.
* Focus on making your **logic understandable quickly**.

---

## Summary

* **Definition**: Non-executable text in code.
* **Symbol**: `#`
* **Purpose**: Improve readability, help teams, and help your future self.
* **Multi-line**: Write `#` at the start of each line (no special block syntax).
* **Best Practice**: Keep comments short and to the point.

---

