
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


# Data Types 

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


# Variables

## 1. What is a Variable?

* **Definition**:
  A variable is a **container** that stores a value for future use.
* Used when you don’t know in advance what value will appear during program execution.
* Example:

  * A login system doesn’t know the user’s name until they log in.
  * Instead of writing the name directly in the program, we use a variable (e.g., `name`) to hold the value.

---

## 2. Why are Variables Fundamental?

* Every programming language uses them.
* Allow **reusability**: one codebase can serve millions of users by substituting values inside variables.
* Example:

  ```python
  a = 5
  b = 10
  print(a + b)
  ```

  Output depends on values stored inside `a` and `b`.

---

## 3. Variables in C vs Python

* **C Example**:

  ```c
  int a = 5;   // must declare type
  ```

  * Once declared as `int`, it can only store integers.
* **Python Example**:

  ```python
  name = "Jobaer"
  print(name)
  ```

  * No need to declare type.
  * Python automatically infers the type.

---

## 4. Key Concepts in Python Variables

### a) Dynamic Typing

* **Definition**:
  In Python, you don’t need to declare the data type.
  The type is inferred automatically from the value assigned.
* Example:

  ```python
  x = "Hello"    # string
  y = 42         # integer
  z = 3.14       # float
  ```
* Contrast: In C/Java, you must specify types explicitly (static typing).

---

### b) Dynamic Binding

* **Definition**:
  A variable in Python is **not permanently bound** to one type.
  Its type can change when a new value is assigned.
* Example:

  ```python
  x = "Hello"   # string
  x = 42        # now integer
  x = True      # now boolean
  ```
* Contrast: In C/Java, once a variable type is declared, it cannot change.

---

## 5. Multiple Variable Assignment

### Method 1 – Multiple in One Line

```python
a = 5; b = 6; c = 7
```

### Method 2 – Tuple Style

```python
a, b, c = 5, 6, 7
```

### Method 3 – Same Value to All

```python
a = b = c = 6
```

---

## 6. Invalid Case Example

* Forgetting quotation marks when storing a string → error.

```python
name = Jobaer   #  Error
name = "Jobaer" #  Correct
```

---

## 7. Summary

* **Variable = container for future values.**
* **Dynamic Typing** → Python automatically infers type.
* **Dynamic Binding** → variable can change type anytime.
* **Multiple Assignments** supported in one line.
* **No declaration needed** before use (unlike C/Java).

---

# Keywords and Identifiers

## 1. Case Sensitivity

* Python is a **case-sensitive programming language**.
* Example:

  * `True` and `true` are different.
  * You cannot interchange upper- and lower-case keywords.

---

## 2. Keywords in Python

* **Definition**:
  Keywords are **reserved words** in Python that have special meaning.
* They are part of the language syntax and **cannot be used as variable names**.
* Example Keywords: `for`, `while`, `if`, `True`, `False`, `import`, `and`, `or`.
* Why?

  * The compiler/interpreter uses them to understand the logic of the program.
  * If you use them as variable names, it creates confusion and errors.
* Example of invalid use:

  ```python
  for = 10   # ❌ invalid, because 'for' is a keyword
  ```
* To see all keywords:

  ```python
  import keyword
  print(keyword.kwlist)
  ```

  * Python has **33 keywords** (in the version referenced).

---

## 3. Identifiers in Python

* **Definition**:
  Identifiers are **names given to variables, functions, classes, modules, or objects**.
* They help us **identify** different parts of a program.

---

## 4. Rules for Naming Identifiers

1. Must start with a **letter** or an **underscore (_)**.

   * ✅ `name`, `_value`
   * ❌ `1name` (cannot start with a digit)
2. Can contain **letters, digits, and underscores**.

   * ✅ `student1`, `first_name`
   * ❌ `first-name` (hyphen not allowed)
3. Cannot include special characters other than underscore.

   * ❌ `score$`
4. Can use double underscore (e.g., `__init__`), but such names often have special meaning in Python.
5. Cannot use **keywords** as identifiers.

   * ❌ `if = 5`
   * ❌ `True = "yes"`

---

## 5. Examples

* ✅ Valid Identifiers:

  ```python
  name = "Alice"
  _value = 10
  student1 = 25
  first_name = "John"
  ```
* ❌ Invalid Identifiers:

  ```python
  1value = 10      # starts with digit
  first-name = 20  # contains hyphen
  for = 15         # reserved keyword
  ```

---

## 6. Key Takeaways

* Keywords = reserved words with predefined meaning.
* Identifiers = names you create for program elements.
* Python is case-sensitive.
* Always follow naming rules: start with letter/underscore, no special characters (except `_`), and never use keywords.

---


# User Input and Type Conversion

## 1️⃣ Introduction

> “Hello guys, welcome to my YouTube channel ‘Python Programming’. In this video, we will cover two topics — **how to take user input** and **type conversion**.”

* In this session, you will learn:

  * How to take **input from a user** in Python.
  * In the next session, you will learn how to **convert data types**.

---

## 2️⃣ Why User Input Is Important

> “If you’ve ever done programming before, you already know that taking input from the user is very important.”

### Two kinds of software:

1. **Static Software (Non-interactive)**

   * Communicates only one-way: *software → user*.
   * The user cannot respond back.
   * **Examples:**

     * Alarm clock

     * Calendar

     * Government websites

     * College portals

     * Blogs

   > “In these, the software talks to you, but you don’t talk back to it.”

---

2. **Dynamic Software (Interactive)**

   * The user and the software communicate **both ways**.
   * The user provides input, and the software responds accordingly.
   * **Examples:**

     * YouTube (you search, comment, like, share)
     * WhatsApp (you send messages)
     * Zomato or Swiggy (you enter address, select food, and confirm orders)

> “Most applications and websites you use today are dynamic. To make dynamic software, taking input from users is essential.”

---

## 3️⃣ Input in Different Programming Languages

Every language provides its own way to accept user input:

| Language | Function/Command  |
| -------- | ----------------- |
| C        | `scanf()`         |
| C++      | `cin`             |
| Java     | `System.in`       |
| PHP      | `$_GET`, `$_POST` |
| Python   | `input()`         |

> “So, all programming languages have a mechanism that allows the programmer to take user input.”

---

## 4️⃣ The `input()` Function in Python

> “In Python, the built-in function for taking input is called **`input()`**.”

* **Definition:**
  `input()` is a built-in function that waits for user input, takes it as text (string), and returns it.

* **Syntax:**

  ```python
  variable = input()
  ```

* When executed:

  * It displays a **prompt box** on the screen.
  * The user types a value and presses Enter.
  * The program stores that value in the variable.

> “It’s very simple and straightforward — no complicated syntax.”

---

## 5️⃣ The Problem with Plain `input()`

If you just call `input()` without any text prompt, it’s unclear what the user should type.

Example:

```python
name = input()
```

The user only sees an empty input line and doesn’t know whether to type a **name, email, or number**.

---

## 6️⃣ Using a Prompt Message

You can pass a message (called a **prompt**) inside the parentheses to tell the user what to enter.

Example:

```python
name = input("Enter your name: ")
```

> “If you run this, the user will see the message *‘Enter your name’*, type their name, and press Enter.”

### Output example:

```
Enter your name: Jobaer
```

Now, `"Jobaer"` is stored inside the variable `name`.

---

### Explanation 

> “Whenever you use `input()`, make sure you tell the user what input you are demanding.”

So, **always provide clear prompts** like:

```python
age = input("Enter your age: ")
email = input("Enter your email address: ")
```

---

## 7️⃣ Writing a Simple Program Using `input()`

Let’s write a program that takes **two numbers from the user** and **prints their sum**.

```python
# taking input from user
first_number = input("Enter the first number: ")
second_number = input("Enter the second number: ")

# printing the input values
print(first_number)
print(second_number)

# adding the numbers
result = first_number + second_number
print("Result:", result)
```

### Output Example:

```
Enter the first number: 56
Enter the second number: 7
Result: 567
```

---

## 8️⃣ The Problem — Why “567” Instead of “63”?

> “Something’s wrong! The output should have been 63, not 567.”

### Explanation:

When you use `input()`, the data you receive from the user is always in **string format**, even if they type numbers.

> “The `input()` function always returns the value in string format.”

So, when you use `+` between two strings, Python **concatenates** them instead of adding.

Example:

```python
"56" + "7"  # → "567"
```

But we wanted:

```python
56 + 7  # → 63
```

---

## 9️⃣ Why Python Takes Input as a String

> “This is a very important property of the `input()` function.”

* When a user types something, Python has to decide what *type* of data it is — text, integer, or something else.
* Converting everything to a **string** is the simplest and safest default option.

### Reason:

> “A string is a universal data format — it can represent any kind of value.”

**For example:**

* A user typing a number → `"56"`
* A user typing text → `"Hello"`
* A user typing a float → `"3.14"`

Everything can be expressed as a string.
But the reverse isn’t always possible — not every text can be converted to a number.

> “You can store `Kolkata` in a string, but you can’t store `Kolkata` in an integer.”

That’s why `input()` always gives you a **string**.

---

##  10 How to Check Data Type

You can check the type of any variable using the built-in **`type()`** function.

### Example:

```python
x = input("Enter something: ")
print(type(x))
```

### Output:

```
Enter something: 45
<class 'str'>
```

---

### More Examples:

| Input       | Code                     | Output              |
| ----------- | ------------------------ | ------------------- |
| `4`         | `print(type(4))`         | `<class 'int'>`     |
| `4.5`       | `print(type(4.5))`       | `<class 'float'>`   |
| `"hello"`   | `print(type("hello"))`   | `<class 'str'>`     |
| `True`      | `print(type(True))`      | `<class 'bool'>`    |
| `6 + 3j`    | `print(type(6 + 3j))`    | `<class 'complex'>` |
| `[1, 2, 3]` | `print(type([1, 2, 3]))` | `<class 'list'>`    |

> “`type()` is a very useful function. We will use it a lot in future topics.”

---

## 11 The Root of the Problem (and What’s Next)

> “Our program doesn’t work because we’re adding strings, not numbers.”

To fix this, we’ll have to **convert data types** manually — for example, convert from string to integer before performing addition.

This process is called **Type Conversion** or **Type Casting**.

---

# ✅ Summary

| Concept                  | Description                                                       | Example                             |
| ------------------------ | ----------------------------------------------------------------- | ----------------------------------- |
| **Static Software**      | Software that only displays information, doesn’t take user input. | Alarm clock, calendar               |
| **Dynamic Software**     | Software that interacts with the user and takes input.            | YouTube, WhatsApp                   |
| **User Input in Python** | Taken using the built-in `input()` function.                      | `name = input("Enter your name: ")` |
| **Prompt Message**       | Text shown to guide the user.                                     | `"Enter your age: "`                |
| **Default Return Type**  | The `input()` function always returns a string (`<class 'str'>`). | `type(input()) → str`               |
| **Type Checking**        | Use `type()` function to know the data type.                      | `type(4.5)` → `<class 'float'>`     |
| **Next Topic**           | Type Conversion (string → int, float, etc.)                       | To be covered next                  |

---
