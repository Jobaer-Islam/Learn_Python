
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

## 1️ Introduction

> “Hello guys, welcome to my YouTube channel ‘Python Programming’. In this video, we will cover two topics — **how to take user input** and **type conversion**.”

* In this session, you will learn:

  * How to take **input from a user** in Python.
  * In the next session, you will learn how to **convert data types**.

---

## 2️ Why User Input Is Important

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

## 3️ Input in Different Programming Languages

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

## 4️ The `input()` Function in Python

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

## 5️ The Problem with Plain `input()`

If you just call `input()` without any text prompt, it’s unclear what the user should type.

Example:

```python
name = input()
```

The user only sees an empty input line and doesn’t know whether to type a **name, email, or number**.

---

## 6️ Using a Prompt Message

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

## 7️ Writing a Simple Program Using `input()`

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

## 8️ The Problem — Why “567” Instead of “63”?

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

## 9️ Why Python Takes Input as a String

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

> “You can store `Dhaka` in a string, but you can’t store `Dhaka` in an integer.”

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

# Summary

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

#  Type Conversion

##  2. What is Type Conversion?

> “Type conversion is a simple process in programming where you convert one data type into another — for example, converting a string into an integer, or an integer into a float.”

###  Definition:

**Type Conversion** is the process of converting the value of one data type into another compatible type.

### Example:

```python
x = "56"
y = int(x)
print(y)      # Output: 56
print(type(y))  # Output: <class 'int'>
```

---

##  3. Rule of Compatibility

> “You can only convert data types if they are compatible.”

Meaning — conversion will only work when it makes sense.

###  Possible Conversions

* `"56"` → `int("56")` → `56`
* `"3.14"` → `float("3.14")` → `3.14`
* `45` → `float(45)` → `45.0`

###  Impossible Conversions

* `"Dhaka"` → `int("Dhaka")` → ❌ **Error**
* `"ringtone"` → `int("ringtone")` → ❌ **Error**

> “You cannot convert text like ‘Dhaka’ into numbers because they are not numerically compatible.”

---

##  4. Two Types of Type Conversion in Python

Python supports **two types** of type conversion:

| Type                         | Who Performs It                      | Also Called     | Description                                                               |
| ---------------------------- | ------------------------------------ | --------------- | ------------------------------------------------------------------------- |
| **Implicit Type Conversion** | Performed automatically by Python    | *Type Coercion* | Python converts one type to another without the programmer’s instruction. |
| **Explicit Type Conversion** | Performed manually by the programmer | *Type Casting*  | The programmer explicitly tells Python which type to convert into.        |

---

##  5. Implicit Type Conversion (Automatic Conversion)

###  Definition:

> “Implicit type conversion happens when Python automatically converts one data type into another compatible type behind the scenes.”

You don’t have to tell Python to do it — it’s done automatically when needed.

---

### Example 1:

```python
x = 4
y = 5.5
result = x + y
print(result)
```

**Explanation:**

* `x` is an integer (`int`)
* `y` is a floating-point number (`float`)

When Python adds them:

* It automatically converts `x` (integer) into a float to perform the addition.
* The result is a float.

**Output:**

```
9.5
```

> “Python is intelligent enough to figure out how to handle this situation without your help.”

---

### Example 2:

```python
x = 5
y = 6
z = x + y + 72
print(z)
```

**Output:**

```
83
```

> “Even though the types differ (integer + integer + integer), Python internally performs implicit conversions as needed to maintain data consistency.”

---

### Example 3: Complex Number Mixing

```python
a = 4
b = 5.5
c = 6 + 3j
print(a + c)
```

**Output:**

```
(10+3j)
```

**Explanation:**

* `a` is an integer, `c` is complex.
* Python automatically converts the integer into complex format before performing the addition.

> “In all these cases, Python automatically figures out how to perform the operation correctly by converting the data types in the background.”

---

### Summary Table: Implicit Conversion

| Operation    | Before          | After Conversion  | Result  |
| ------------ | --------------- | ----------------- | ------- |
| `4 + 5.5`    | int + float     | float + float     | 9.5     |
| `5 + 6 + 72` | int + int + int | all int           | 83      |
| `4 + (6+3j)` | int + complex   | complex + complex | (10+3j) |

---

##  6. When Implicit Conversion Doesn’t Work

> “There are scenarios where Python cannot automatically decide what to do — and in such cases, you must manually instruct it.”

For example, consider this code from the earlier video:

```python
first = input("Enter first number: ")
second = input("Enter second number: ")
result = first + second
print(result)
```

**Output:**

```
Enter first number: 45
Enter second number: 67
4567
```

> “Here, both inputs were strings. Python thought it should concatenate them instead of adding.”

Python cannot automatically convert these to integers because:

* It doesn’t know if `"45"` and `"67"` are numbers or text.
* Only you, the programmer, can tell that.

Hence, we use **Explicit Type Conversion.**

---

##  7. Explicit Type Conversion (Manual Conversion)

###  Definition:

> “Explicit type conversion happens when the programmer manually instructs Python to convert a value from one type to another.”

You use **built-in conversion functions** like:

* `int()`
* `float()`
* `complex()`
* `str()`
* `list()`
* `set()`
* `dict()`
* `tuple()`

---

### Example 1 – Using `int()` Function

```python
x = "45"
y = int(x)
print(y)
print(type(y))
```

**Output:**

```
45
<class 'int'>
```

> “The `int()` function takes a compatible value and converts it into an integer.”

---

### Example 2 – `int()` with Float

```python
x = 4.5
y = int(x)
print(y)
```

**Output:**

```
4
```

> “`int()` converted the float 4.5 into 4. The decimal part was removed (truncated).”

---

### Example 3 – `int()` with String Numbers

```python
x = "123"
print(int(x))
```

**Output:**

```
123
```

> “When the string contains only digits, conversion works perfectly.”

But:

```python
print(int("Hello"))
```

will raise an error  because it’s not a number.

---

### Example 4 – Using `float()` Function

```python
x = 4
print(float(x))
```

**Output:**

```
4.0
```

> “The `float()` function converts integers or strings (that represent numbers) into floating-point numbers.”

---

### Example 5 – Using `complex()` Function

```python
x = 4
print(complex(x))
```

**Output:**

```
(4+0j)
```

> “The `complex()` function converts numbers into complex format. Here, `4` became `(4+0j)`.”

---

### Example 6 – Using `list()` Function

```python
x = "Hello"
print(list(x))
```

**Output:**

```
['H', 'e', 'l', 'l', 'o']
```

> “`list()` takes an iterable like a string and converts it into a list of characters.”

---

### Example 7 – Using `set()` Function

```python
x = "Hello"
print(set(x))
```

**Output (order may vary):**

```
{'H', 'e', 'l', 'o'}
```

> “`set()` converts a sequence into a set of unique elements.”

---

### Example 8 – Using `dict()` Function

You can use `dict()` with key–value pairs:

```python
x = [("a", 1), ("b", 2)]
print(dict(x))
```

**Output:**

```
{'a': 1, 'b': 2}
```

> “`dict()` converts a list of tuples into a dictionary — but only when each item is a valid key-value pair.”

---

###  Invalid Conversions

> “You can’t convert every value into every data type.”

Examples:

```python
int("Dhaka")   #  Error
float("abcd")    #  Error
list(45)         #  Error (integers are not iterable)
```

These fail because the data is not **compatible** with the target type.

---

##  8. Temporary Nature of Type Conversion

> “Type conversion is not a permanent operation.”

It doesn’t modify the original variable; it creates a **new value** of the converted type.

---

### Example:

```python
a = 4.5
b = int(a)
print(b)  # 4
print(a)  # 4.5
```

**Explanation:**

* You converted `a` to an integer and stored it in `b`.
* But `a` itself is still a float.

> “When you apply conversion, Python creates a new converted value. The original variable stays unchanged.”

---

##  9. Type Casting vs Type Conversion

> “You may have heard of type casting in other programming languages.”

| Concept             | Nature    | Description                                                                           |
| ------------------- | --------- | ------------------------------------------------------------------------------------- |
| **Type Casting**    | Permanent | Changes the data type of a variable (common in languages like C or Java).             |
| **Type Conversion** | Temporary | Does not modify the original variable; it creates a converted copy (Python behavior). |

So:

> “Type Casting is permanent.
> Type Conversion is not permanent.”

---

##  10. Fixing the Old Program (Final Solution)

Let’s revisit our earlier problem — adding two numbers entered by the user.

###  Wrong Version (Without Conversion)

```python
a = input("Enter first number: ")
b = input("Enter second number: ")
result = a + b
print(result)
```

Output:

```
Enter first number: 45
Enter second number: 67
4567
```

###  Correct Version (With Conversion)

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
result = a + b
print("Result:", result)
```

Output:

```
Enter first number: 45
Enter second number: 67
Result: 112
```

> “Our problem is solved! By converting the input into integers, we performed proper mathematical addition.”

---

##  11. Best Practice — Convert at the Input Stage

> “If you perform conversion right when taking input, you’ll avoid repeating the conversion in multiple places.”

### Instead of:

```python
a = input("Enter number: ")
a = int(a)
```

### Do this:

```python
a = int(input("Enter number: "))
```

> “This way, you only convert once — and all future mathematical operations will work correctly.”

---

##  12. Why Conversion Matters in Real Projects

> “You will often need to perform type conversion in real-world projects — especially when working with user input, databases, APIs, or file data.”

For example:

* Reading a CSV file → numbers are read as strings → must convert to integers/floats.
* Accepting user input for price, quantity, or marks → must convert to numeric types before processing.
* Converting floats to integers when rounding values or computing indices.

> “So always remember, type conversion is not just for learning — it’s a very practical concept you’ll use often.”

---

##  13. Quick Summary

| Concept                 | Description                                                                      | Example                              |
| ----------------------- | -------------------------------------------------------------------------------- | ------------------------------------ |
| **Type Conversion**     | Changing a value from one data type to another.                                  | `int("45") → 45`                     |
| **Implicit Conversion** | Performed automatically by Python.                                               | `4 + 5.5 → 9.5`                      |
| **Explicit Conversion** | Done manually using functions.                                                   | `int("56") → 56`                     |
| **Common Functions**    | `int()`, `float()`, `complex()`, `str()`, `list()`, `set()`, `dict()`, `tuple()` |                                      |
| **Compatibility Rule**  | Only possible for compatible data.                                               | `"123"` → int ✅; `"Dhaka"` → int ❌ |
| **Temporary Nature**    | Original value remains unchanged.                                                | `a=4.5; int(a)` → `a` still 4.5      |
| **Best Practice**       | Convert at the input stage.                                                      | `a = int(input("Enter number: "))`   |

---

##  14. Full Example — Final Program

```python
# Program: Add Two Numbers with Type Conversion

# Taking input from user and converting to integers immediately
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))

# Performing addition
sum_result = num1 + num2

# Displaying result
print("The sum is:", sum_result)
```

### Output:

```
Enter the first number: 56
Enter the second number: 7
The sum is: 63
```

> “This is the correct and clean way to handle numeric input in Python.”

---

##  15. Final Thoughts

* Type conversion ensures your program behaves as expected when handling user input or external data.
* Always check **data compatibility** before conversion to avoid errors.
* Remember that **conversion is temporary**, and **type casting is permanent** (in other languages).
* Python provides **built-in functions** to make conversion easy.
* Best practice: Convert at the point of input to simplify your code and avoid repetitive conversions.

---


#  Literals and Operators 

> *“In programming, before we can manipulate data, we need to represent it — and that’s where **literals** come in. Once we have data, we perform operations on it — and that’s where **operators** come into play.”*

---

##  1. What Are Literals?

A **literal** is a fixed value assigned directly to a variable or used in an expression.

**Definition:**

> A literal in Python is a raw value given to a variable or constant. It directly represents data.

**Example:**

```python
x = 10       # Integer literal
name = "John" # String literal
flag = True   # Boolean literal
```

Python supports **four main categories of literals:**

1. **Numeric Literals**
2. **String Literals**
3. **Boolean Literals**
4. **Special Literals**

Let’s dive into each.

---

##  2. Numeric Literals

Numeric literals represent numbers. In Python, there are **three types:**

| Type        | Description                           | Example      |
| ----------- | ------------------------------------- | ------------ |
| **int**     | Whole numbers (no decimal)            | `x = 42`     |
| **float**   | Numbers with decimal points           | `y = 3.14`   |
| **complex** | Numbers with real and imaginary parts | `z = 2 + 3j` |

Let’s look at these one by one.

---

### 2.1  Integer Literals

**Integers** are whole numbers (positive, negative, or zero).

Example:

```python
a = 210
print(a)  # Output: 210
```

By default, integers are written in **decimal (base 10)**, but Python also supports **binary**, **octal**, and **hexadecimal** representations.

---

#### (a) Binary Literals

Binary literals are prefixed with `0b` or `0B`.

```python
a = 0b1010
print(a)  # Output: 10 (decimal)
```

> “In electronics or embedded programming (like Raspberry Pi), binary values are common for controlling pins, sensors, or motors.”

Example (real use):

```python
motor_signal = 0b1101  # 13 in decimal
```

---

#### (b) Octal Literals

Octal literals use the prefix `0o` or `0O`.

```python
b = 0o12
print(b)  # Output: 10 (decimal)
```

Octal is rarely used in everyday Python, but still valid for low-level programming.

---

#### (c) Hexadecimal Literals

Hexadecimal literals are prefixed with `0x` or `0X`.

```python
c = 0x1F
print(c)  # Output: 31 (decimal)
```

> Hex is often used in color codes, memory addresses, and binary data representation.

Example:

```python
color_code = 0xFF5733  # Hex for an orange shade
```

---

### 2.2  Float Literals

Float literals contain decimal points or use **scientific notation**.

Example (normal float):

```python
pi = 3.14159
```

Example (scientific notation):

```python
large = 1.5e2   # 1.5 × 10² = 150.0
small = 1.5e-3  # 1.5 × 10⁻³ = 0.0015
```

**Scientific notation** is extremely useful for:

* Very large or small numbers
* Scientific calculations
* NASA or biomedical data (e.g., viral concentration, light intensity)

---

### 2.3  Complex Literals

Complex numbers include a **real** and an **imaginary** part (with `j`).

Example:

```python
z = 3 + 5j
print(z)         # (3+5j)
print(z.real)    # 3.0
print(z.imag)    # 5.0
```

> “Useful in mathematics, signal processing, and physics simulations.”

---

### 2.4  Numeric Summary

| Type        | Example                 | Description           |
| ----------- | ----------------------- | --------------------- |
| Decimal     | `x = 25`                | Base 10 integer       |
| Binary      | `y = 0b1101`            | Base 2 integer        |
| Octal       | `z = 0o17`              | Base 8 integer        |
| Hexadecimal | `c = 0x1F`              | Base 16 integer       |
| Float       | `p = 3.14`, `q = 2.5e3` | Decimal or scientific |
| Complex     | `r = 2 + 4j`            | Real + imaginary      |

---

##  3. String Literals

String literals represent sequences of characters enclosed in quotes.

Python allows **three main ways** to create strings:

| Syntax        | Example                                | Use Case                        |
| ------------- | -------------------------------------- | ------------------------------- |
| Single quotes | `'Hello'`                              | Simple strings                  |
| Double quotes | `"World"`                              | Same as single quotes; flexible |
| Triple quotes | `'''Multiline'''` or `"""Multiline"""` | Multiline text                  |

---

### 3.1  Single-quoted Strings

```python
msg = 'Hello World'
print(msg)
```

---

### 3.2  Double-quoted Strings

```python
greet = "I'm learning Python"
print(greet)
```

> Use double quotes when the text itself contains single quotes — to avoid escape sequences.

---

### 3.3  Triple-quoted Strings (Multiline)

Triple quotes (`'''` or `"""`) are ideal for **multi-line text** like paragraphs, HTML, or documentation.

```python
para = """This is a
multi-line
string in Python."""
print(para)
```

Use cases:

* Docstrings
* Blog text
* Email or long messages

---

### 3.4  Unicode Strings

Python natively supports Unicode characters like emojis and symbols.

Use the prefix **`u`** to indicate a Unicode string (mainly for legacy Python 2 compatibility).

Example:

```python
smile = u"\u263A"
heart = u"\u2764"
print(smile, heart)
```

Output:

```
☺ ❤
```

> Unicode ensures Python can handle international languages, emojis, and special symbols.

---

### 3.5  Raw Strings

Raw strings are prefixed with **`r`** to prevent escape sequences (like `\n`, `\t`) from being processed.

```python
path = r"C:\new_folder\test"
print(path)
```

Output:

```
C:\new_folder\test
```

> “Raw strings are especially useful when writing regular expressions, file paths, or HTML code containing many backslashes.”

---

### 3.6  Summary: String Literals

| Type    | Syntax       | Example               | Output    |
| ------- | ------------ | --------------------- | --------- |
| Single  | `'text'`     | `'hello'`             | hello     |
| Double  | `"text"`     | `"world"`             | world     |
| Triple  | `'''text'''` | multiline text        | multiline |
| Unicode | `u"❤"`       | emoji or symbol       | ❤         |
| Raw     | `r"text\n"`  | raw text (no escapes) | text\n    |

---

##  4. Boolean Literals

Boolean literals represent **truth values** — either `True` or `False`.

```python
is_ready = True
is_logged_in = False
```

In Python, `True` and `False` are internally treated as integers:

* `True` → `1`
* `False` → `0`

Example:

```python
print(True + True)   # 2
print(True + False)  # 1
print(False + False) # 0
```

> “Here, type conversion automatically happens — Python internally treats boolean values as integers when required.”

Boolean literals are heavily used in:

* Condition checks (`if`, `while`)
* Logical expressions
* Decision-making systems

---

##  5. Special Literal – `None`

The **special literal** `None` represents the **absence of a value** or a **null reference**.

```python
data = None
print(data)  # Output: None
```

> “It means ‘nothing’ or ‘no value yet’. You’ll often see `None` in default arguments, function returns, and variable initialization.”

---

### 5.1  Why Use `None`?

In Python, you **cannot declare variables without assigning a value.**

Example:

```python
x
```

Output:

```
NameError: name 'x' is not defined
```

To declare an empty variable (no value yet):

```python
x = None
```

Now you can safely use `x` later.

> “This is like reserving a placeholder in memory until a real value arrives.”

---

### 5.2  Real-World Example

```python
user_email = None
if user_email is None:
    print("No email assigned yet.")
else:
    print(user_email)
```

Output:

```
No email assigned yet.
```

---

##  6. Quick Summary of Literals

| Type    | Description               | Example              |
| ------- | ------------------------- | -------------------- |
| Numeric | Integers, floats, complex | `10`, `3.14`, `2+3j` |
| String  | Text enclosed in quotes   | `'Hello'`, `"World"` |
| Boolean | Truth values              | `True`, `False`      |
| Special | Represents null value     | `None`               |

---

#  7. Python Operators

Now that we can store data (literals), the next step is to **manipulate it** — and that’s done using **operators**.

**Definition:**

> Operators are special symbols or keywords that perform operations on variables and values.

---

##  8. Types of Operators in Python

Python provides several categories of operators:

| Type                                  | Description                     | Examples                                 |                         |
| ------------------------------------- | ------------------------------- | ---------------------------------------- | ----------------------- |
| **Arithmetic Operators**              | Perform mathematical operations | `+`, `-`, `*`, `/`, `%`, `**`, `//`      |                         |
| **Comparison (Relational) Operators** | Compare two values              | `==`, `!=`, `>`, `<`, `>=`, `<=`         |                         |
| **Logical Operators**                 | Combine multiple conditions     | `and`, `or`, `not`                       |                         |
| **Assignment Operators**              | Assign values to variables      | `=`, `+=`, `-=`, `*=`, `/=`, `//=`, `%=` |                         |
| **Bitwise Operators**                 | Perform bit-level operations    | `&`, `                                   | `, `^`, `~`, `<<`, `>>` |
| **Membership Operators**              | Test membership in sequences    | `in`, `not in`                           |                         |
| **Identity Operators**                | Test object identity            | `is`, `is not`                           |                         |

Let’s study them one by one.

---

##  9. Arithmetic Operators

Used for mathematical calculations.

| Operator | Description         | Example  | Output |
| -------- | ------------------- | -------- | ------ |
| `+`      | Addition            | `3 + 2`  | 5      |
| `-`      | Subtraction         | `5 - 3`  | 2      |
| `*`      | Multiplication      | `4 * 2`  | 8      |
| `/`      | Division            | `5 / 2`  | 2.5    |
| `%`      | Modulus (remainder) | `5 % 2`  | 1      |
| `**`     | Exponentiation      | `2 ** 3` | 8      |
| `//`     | Floor division      | `5 // 2` | 2      |

### Example:

```python
a, b = 10, 3
print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a % b)
print(a ** b)
print(a // b)
```

---

##  10. Comparison Operators

Used to compare values. The result is always **Boolean** (`True` or `False`).

| Operator | Description      | Example  | Output |
| -------- | ---------------- | -------- | ------ |
| `==`     | Equal to         | `5 == 5` | True   |
| `!=`     | Not equal to     | `5 != 3` | True   |
| `>`      | Greater than     | `5 > 3`  | True   |
| `<`      | Less than        | `3 < 5`  | True   |
| `>=`     | Greater or equal | `5 >= 5` | True   |
| `<=`     | Less or equal    | `3 <= 5` | True   |

Example:

```python
a, b = 10, 20
print(a == b)
print(a != b)
print(a > b)
print(a < b)
print(a >= b)
print(a <= b)
```

---

##  11. Logical Operators

Used to combine conditional statements.

| Operator | Description             | Example            | Output |
| -------- | ----------------------- | ------------------ | ------ |
| `and`    | True if both are True   | `x > 5 and y < 10` | True   |
| `or`     | True if any one is True | `x > 5 or y < 10`  | True   |
| `not`    | Negates the result      | `not(x > 5)`       | False  |

Example:

```python
x, y = 7, 3
print(x > 5 and y < 10)   # True
print(x > 10 or y < 5)    # True
print(not(x > 5))         # False
```

---

##  12. Assignment Operators

Used to assign values or modify existing values.

| Operator | Example   | Equivalent to |
| -------- | --------- | ------------- |
| `=`      | `a = 5`   | Assign 5      |
| `+=`     | `a += 2`  | `a = a + 2`   |
| `-=`     | `a -= 3`  | `a = a - 3`   |
| `*=`     | `a *= 4`  | `a = a * 4`   |
| `/=`     | `a /= 2`  | `a = a / 2`   |
| `//=`    | `a //= 3` | `a = a // 3`  |
| `%=`     | `a %= 2`  | `a = a % 2`   |
| `**=`    | `a **= 2` | `a = a ** 2`  |

Example:

```python
a = 10
a += 5   # a = 15
a *= 2   # a = 30
print(a)
```

---

##  13. Bitwise Operators

Work at the binary (bit) level.

| Operator | Meaning     | Example    | Result |    |     |
| -------- | ----------- | ---------- | ------ | -- | --- |
| `&`      | Bitwise AND | `5 & 3`    | `1`    |    |     |
| `        | `           | Bitwise OR | `5     | 3` | `7` |
| `^`      | Bitwise XOR | `5 ^ 3`    | `6`    |    |     |
| `~`      | Bitwise NOT | `~5`       | `-6`   |    |     |
| `<<`     | Left shift  | `5 << 1`   | `10`   |    |     |
| `>>`     | Right shift | `5 >> 1`   | `2`    |    |     |

> “These operators are used in digital logic, image processing, and low-level computation.”

---

##  14. Membership Operators

Used to test if a value exists in a sequence (like list, tuple, or string).

| Operator | Example              | Output |
| -------- | -------------------- | ------ |
| `in`     | `'a' in 'apple'`     | True   |
| `not in` | `'z' not in 'apple'` | True   |

Example:

```python
fruits = ['apple', 'banana', 'cherry']
print('apple' in fruits)      # True
print('mango' not in fruits)  # True
```

---

##  15. Identity Operators

Used to compare **object identities**, not just values.

| Operator | Example      | Output                    |
| -------- | ------------ | ------------------------- |
| `is`     | `x is y`     | True if same object       |
| `is not` | `x is not y` | True if different objects |

Example:

```python
x = [1, 2, 3]
y = x
z = [1, 2, 3]
print(x is y)      # True (same object)
print(x is z)      # False (different object, same content)
```

> “Even if two lists look identical, they are different objects unless they point to the same memory address.”

---

##  16. Summary of Operators

| Category   | Examples             | Purpose                        |                     |
| ---------- | -------------------- | ------------------------------ | ------------------- |
| Arithmetic | `+ - * / % ** //`    | Math operations                |                     |
| Comparison | `== != > < >= <=`    | Compare values                 |                     |
| Logical    | `and or not`         | Combine conditions             |                     |
| Assignment | `= += -= *= /=` etc. | Assign/modify variables        |                     |
| Bitwise    | `&                   | ^ ~ << >>`                     | Binary manipulation |
| Membership | `in`, `not in`       | Check presence in a collection |                     |
| Identity   | `is`, `is not`       | Compare object identity        |                     |

---

##  17. Real-Life Examples

### Example 1 – Discount Calculation

```python
price = float(input("Enter price: "))
discount = 10  # percent

if price > 1000:
    price -= price * discount / 100

print("Final price:", price)
```

> Uses arithmetic, comparison, and assignment operators together.

---

### Example 2 – Login Validation

```python
username = "admin"
password = "1234"

u = input("Enter username: ")
p = input("Enter password: ")

if u == username and p == password:
    print("Access granted")
else:
    print("Access denied")
```

> Demonstrates comparison and logical operators.

---

### Example 3 – Membership + Identity

```python
emails = ["a@x.com", "b@y.com"]
new_email = "c@z.com"

if new_email not in emails:
    emails.append(new_email)

print(emails)
```

---

##  18. Key Takeaways

1. **Literals** are fixed values directly written in code.
2. **Types of literals:** Numeric, String, Boolean, Special (`None`).


3. **Operators** act on literals and variables to perform actions.
4. You can use **implicit conversions** (automatic) and **explicit conversions** (manual) when needed.
5. Learn to combine operators logically to write smarter programs.

---

##  19. Final Mini Quiz

1. What is a literal in Python?
2. What are the four types of literals?
3. What is the output of `0b1010`?
4. What does `r"Hello\nWorld"` print?
5. What is the result of `True + False`?
6. Which operator is used for exponentiation?
7. What does `a is b` check?
8. How is `None` different from `False`?

(Answers: 1-Value given to a variable; 2-Numeric, String, Boolean, Special; 3-10; 4-Hello\nWorld; 5-1; 6-`**`; 7-Object identity; 8-`None` = no value, `False` = boolean zero.)

---

# **Decision Control Statements (IF / ELIF / ELSE)**

##  **1. Why Do We Need Decision Making in Programming?**

Your program **usually runs top to bottom**, line by line.
But real-world logic is not always linear — sometimes your program needs to choose **between multiple possible paths**.

This situation is called **branching**.

###   Why branching is needed?

Because sometimes:

* A user may give the correct credentials
* Or the user may give incorrect details
* And in some cases, the user may give **partially correct** details (correct email but wrong password)

Each outcome requires a different response.

So Python needs a mechanism to make decisions.
This mechanism is the **if / elif / else** structure.

---

#  **2. What is an IF Statement?**

###   Definition (Clean English)

> An **if statement** is used when the program needs to check a condition and execute a block of code only if that condition is true.

###   Real example from transcript

Login system:

* If the user enters correct email and password → show **Welcome**
* Else → show **Incorrect credentials**

This is the simplest use-case of decision-making.

---

#  **3. Building a Simple Login System (Base Version)**

*(Based directly on the transcript example)*

We first ask the user for:

* Email
* Password

Then compare them with **predefined correct credentials**.

###   Step 1 — Get Input from User

```python
email = input("Enter your email: ")
password = input("Enter your password: ")
```

###   Step 2 — Store Correct Credentials

```python
correct_email = "example@gmail.com"
correct_password = "1234"
```

###   Step 3 — Apply IF + AND Operator

```python
if email == correct_email and password == correct_password:
    print("Welcome!")
else:
    print("Incorrect credentials")
```

###  Explanation

* `email == correct_email` → checks whether the user entered the correct email
* `password == correct_password` → checks password
* `and` ensures **both must be true**
* If either is wrong → else block executes

---

#  **4. Understanding INDENTATION (VERY IMPORTANT in Python)**

Transcript explanation:

> In Python, you do not use braces `{}` like other languages.
> Instead, indentation decides which lines belong to which block.

###   Example of correct indentation:

```python
if email == correct_email:
    print("Email match")  # inside IF block
print("Done")             # outside IF block
```

Python will throw errors or behave incorrectly if indentation is wrong.

---

#  **5. Adding Complexity — ELIF (Else If)**

Your manager now wants:

* If email is correct but password is wrong → give user **one more chance**
* If user fails again → show error
* If email and password both correct → welcome
* If email itself is wrong → directly reject

Now we have **three cases**:

1. Fully correct
2. Fully wrong
3. Partially correct (correct email but wrong password)

###   Structure:

```
if condition1:
    ...
elif condition2:
    ...
else:
    ...
```

---

#  **6. Implementing ELIF Logic **

###   Step 1 — Basic IF block

```python
if email == correct_email and password == correct_password:
    print("Welcome!")
```

###   Step 2 — ELIF for partial correctness

We check:

* Email is correct
* Password is wrong

To check wrong password, we use `not`.

```python
elif email == correct_email and password != correct_password:
    print("Password incorrect")
    password = input("Enter password again: ")

    # now check again
    if password == correct_password:
        print("Welcome!")
    else:
        print("Incorrect again")
```

###   Step 3 — Final ELSE block

```python
else:
    print("Incorrect credentials")
```

###   Full Code (Updated Login System)

```python
email = input("Enter your email: ")
password = input("Enter your password: ")

correct_email = "example@gmail.com"
correct_password = "1234"

if email == correct_email and password == correct_password:
    print("Welcome!")

elif email == correct_email and password != correct_password:
    print("Password incorrect")
    password = input("Enter password again: ")

    if password == correct_password:
        print("Welcome!")
    else:
        print("Incorrect again")

else:
    print("Incorrect credentials")
```

---

#  **7. Nested IF (IF inside IF)**

Transcript says:

> “When you are already inside an elif block, and again need branching, you can add an IF statement inside. This is called nested IF.”

###   Why use nested IF?

Because after the second chance, we again have two possibilities:

* Password correct
* Password still wrong

###   Example (already shown above)

```python
elif email == correct_email and password != correct_password:
    print("Password incorrect")

    password = input("Enter again: ")

    if password == correct_password:
        print("Welcome!")
    else:
        print("Incorrect again")
```

---

#  **8. Adding Error Checking: Valid Email Format**

Manager now wants additional validation:

> “If the user does not include `@` in the email, then immediately show 'Invalid Email', without asking for password.”

We check:

```python
if '@' not in email:
    print("Invalid email format")
```

###   Then we put remaining logic under ELSE:

```python
if '@' not in email:
    print("Invalid email format")

else:
    # rest of login code goes here
    if email == correct_email and password == correct_password:
        ...
```

###   Full Enhanced Code

*(Final version as described in transcript)*

```python
email = input("Enter your email: ")

if '@' not in email:
    print("Invalid email format")

else:
    password = input("Enter your password: ")

    correct_email = "example@gmail.com"
    correct_password = "1234"

    if email == correct_email and password == correct_password:
        print("Welcome!")

    elif email == correct_email and password != correct_password:
        print("Password incorrect")
        password = input("Enter password again: ")

        if password == correct_password:
            print("Welcome!")
        else:
            print("Incorrect again")

    else:
        print("Incorrect credentials")
```

---

#  **9. Summary of Concepts Learned**

###   IF Statement

Used to check a condition and run code only if condition is true.

###   ELSE

Runs when IF condition fails.

###   ELIF

Used to introduce additional conditions **between** IF and ELSE.

###   NESTED IF

IF inside another IF/ELIF block.

###   LOGICAL OPERATORS

Used heavily in decision-making:

* `and`
* `or`
* `not`

###   MEMBERSHIP TEST

Used to check for characters inside strings:

```python
"@" in email
```

###   Indentation

Defines code blocks in Python.

---

#  **10. Real-Life Understanding **

* Login systems
* Permission checks
* Banking OTP validation
* Form validation
* Payment gateways
* Game logic (e.g., health > 0 → continue playing)

Every modern app depends heavily on **if-elif-else**.

---





