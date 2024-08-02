[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15496150&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

   Python is a high-level, interpreted programming language known for its readability, simplicity, and versatility. Developed by Guido van Rossum and first released in 1991, Python emphasizes code readability and allows developers to express concepts in fewer lines of code compared to other programming languages.

Key Features of Python

1. Readable and Simple Syntax:
   - Python's syntax is clear and easy to understand, which makes it an excellent choice for beginners. The use of indentation to define code blocks enhances readability.
   - Example:
     ```python
     for i in range(5):
         print(i)
     ```

2. Interpreted Language:
   - Python is an interpreted language, meaning that code is executed line by line, which simplifies debugging and development.
   
3. Dynamically Typed:
   - Variable types are determined at runtime, which provides flexibility in coding. For example:
     ```python
     x = 10  # integer
     x = "Hello"  # string
     ```

4. Extensive Standard Library:
   - Python comes with a rich set of libraries and modules that handle a wide range of tasks, from file I/O to web development and data manipulation.
   - Example: Using `math` module:
     ```python
     import math
     print(math.sqrt(16))  # Outputs: 4.0
     ```

5. Cross-Platform:
   - Python is cross-platform and works on various operating systems, including Windows, macOS, and Linux.

6. Object-Oriented and Functional Programming:
   - Python supports multiple programming paradigms, including object-oriented, functional, and procedural programming.
   - Example of a class definition:
     ```python
     class Dog:
         def __init__(self, name):
             self.name = name

         def bark(self):
             return "Woof!"

     dog = Dog("Buddy")
     print(dog.bark())  # Outputs: Woof!
     ```

7. Large Community and Ecosystem:
   - Python has a vast community and a large ecosystem of third-party libraries and frameworks that facilitate various types of development, including web, data science, and automation.

8. Integration Capabilities:
   - Python integrates well with other languages and technologies. It can call C/C++ code and be used for scripting and automating tasks.
   - Example: Using `ctypes` to call a C function:
     ```python
     import ctypes

     libc = ctypes.CDLL("libc.so.6")
     libc.printf(b"Hello from C!\n")
     ```

Use Cases Where Python is Particularly Effective

1. Web Development:
   - Frameworks like Django and Flask make it easy to develop robust web applications. Python's simplicity and powerful libraries streamline backend development.
   - Example:
     ```python
     # Using Flask to create a simple web app
     from flask import Flask
     app = Flask(__name__)

     @app.route('/')
     def home():
         return 'Hello, Flask!'

     if __name__ == '__main__':
         app.run()
     ```

2. Data Science and Machine Learning:
   - Python is widely used for data analysis, machine learning, and scientific computing, thanks to libraries like Pandas, NumPy, SciPy, and Scikit-learn.
   - Example:
     ```python
     import pandas as pd
     data = pd.read_csv('data.csv')
     print(data.head())
     ```

3. Automation and Scripting:
   - Python is an excellent choice for automating repetitive tasks, such as file manipulation, web scraping, and system administration.
   - Example: Web scraping with BeautifulSoup:
     ```python
     from bs4 import BeautifulSoup
     import requests

     response = requests.get('http://example.com')
     soup = BeautifulSoup(response.text, 'html.parser')
     print(soup.title.text)
     ```

4. Game Development:
   - Libraries like Pygame allow for game development in Python, providing tools for creating 2D games.
   - Example:
     ```python
     import pygame
     pygame.init()
     screen = pygame.display.set_mode((640, 480))
     pygame.display.set_caption("Hello, Pygame!")
     ```

5. Scientific Computing:
   - Python's scientific libraries, such as SciPy and SymPy, are used for complex mathematical calculations, simulations, and symbolic mathematics.
   - Example:
     ```python
     from sympy import symbols, solve

     x = symbols('x')
     equation = x**2 - 4
     solutions = solve(equation, x)
     print(solutions)  # Outputs: [-2, 2]
     ```

6. Networking:
   - Python's libraries, such as Twisted and Socket, facilitate the creation of network applications and services.
   - Example:
     ```python
     import socket

     s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
     s.connect(("example.com", 80))
     s.send(b"GET / HTTP/1.1\r\nHost: example.com\r\n\r\n")
     print(s.recv(1024))
     ```

2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.

   Here are the steps to install Python on Windows, along with how to verify the installation and set up a virtual environment:

Installing Python on Windows

1. Download the Installer:
   - Go to the [Python official website](https://www.python.org/downloads/).
   - Click on the "Download Python" button for the latest version (e.g., Python 3.x.x).

2. Run the Installer:
   - Open the downloaded `.exe` file.
   - **Important**: Check the box that says "Add Python 3.x to PATH" before clicking "Install Now."
   - Click "Install Now" and follow the prompts.

3. Verify the Installation:
   - Open Command Prompt (cmd) or PowerShell.
   - Run the following commands:
     ```bash
     python --version
     ```
     ```bash
     pip --version
     ```
   - Both commands should display the installed version of Python and pip.

4. Set Up a Virtual Environment:
   - Open Command Prompt or PowerShell.
   - Navigate to your project directory or create one:
     ```bash
     mkdir my_project
     cd my_project
     ```
   - Create a virtual environment:
     ```bash
     python -m venv venv
     ```
   - Activate the virtual environment:
     - **Command Prompt**:
       ```bash
       venv\Scripts\activate
       ```
     - **PowerShell**:
       ```bash
       .\venv\Scripts\Activate
       ```
Using the Virtual Environment

Once the virtual environment is activated, you can install packages using `pip` and they will be isolated from the system-wide Python installation. For example:

```bash
pip install requests
```

To deactivate the virtual environment, simply run:

```bash
deactivate
```

This ensures that the environment is specific to your project and doesn’t interfere with other projects or system-wide packages.
   

3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.

    Here’s a simple Python program that prints "Hello, World!" to the console:

```python
print("Hello, World!")
```

### **Explanation of Basic Syntax Elements**

1. `print()` Function:
   - **Purpose**: The `print()` function outputs text to the console. It is a built-in function in Python.
   - **Usage**: In this example, `print()` is used to display the string `"Hello, World!"`.
   - **Syntax**: `print(<expression>)` where `<expression>` is any valid Python expression that evaluates to a value to be printed.

2. String Literal:
   - **Purpose**: `"Hello, World!"` is a string literal. It is a sequence of characters enclosed in double quotes.
   - **Usage**: String literals are used to represent text in Python. They can be enclosed in single quotes (`'Hello, World!'`) or double quotes (`"Hello, World!"`).

3. Parentheses `()`:
   - **Purpose**: Parentheses are used in Python to call functions and group expressions.
   - **Usage**: In the `print()` function, parentheses enclose the arguments (in this case, the string `"Hello, World!"`).

4. No Semicolons:
   - **Purpose**: Unlike some other languages, Python does not require semicolons at the end of statements.
   - **Usage**: The absence of semicolons is a part of Python's emphasis on readability and simplicity.

Additional Points

- **Indentation**: Python uses indentation to define code blocks, but in this simple example, there is no need for indentation.
- **Comments**: You can add comments in Python using the `#` symbol, which is not present in this simple example but useful for explaining code.

Here’s a slightly extended example with a comment:

```python
# This program prints "Hello, World!" to the console
print("Hello, World!")
```

In this extended example, the `#` symbol starts a comment, which is ignored by the Python interpreter but can be used to provide explanations or notes within the code.

This program is a basic example of Python syntax and semantics, showcasing how simple and readable Python code can be.

4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.

   Python supports several basic data types, each serving different purposes. Here’s a brief overview of the fundamental data types and a script demonstrating their use:

Basic Data Types in Python

1. Integer (`int`):
   - Represents whole numbers without decimal points.
   - Example: `42`, `-7`, `0`

2. Floating-Point (`float`):
   - Represents numbers with decimal points.
   - Example: `3.14`, `-0.001`, `2.0`

3. String (`str`):
   - Represents sequences of characters enclosed in single quotes (`'`) or double quotes (`"`).
   - Example: `'Hello, World!'`, `"Python is fun!"`

4. Boolean (`bool`):
   - Represents truth values: `True` or `False`.
   - Example: `True`, `False`

5. List (`list`):
   - Represents an ordered collection of items that can be of different data types.
   - Lists are mutable (i.e., they can be changed after creation).
   - Example: `[1, 2, 3]`, `['apple', 'banana', 'cherry']`

6. Tuple (`tuple`):
   - Represents an ordered collection of items that can be of different data types.
   - Tuples are immutable (i.e., they cannot be changed after creation).
   - Example: `(1, 2, 3)`, `('apple', 'banana', 'cherry')`

7. Dictionary (`dict`):
   - Represents a collection of key-value pairs.
   - Dictionaries are mutable.
   - Example: `{'name': 'Alice', 'age': 30}`, `{1: 'one', 2: 'two'}`

8. Set (`set`):
   - Represents an unordered collection of unique items.
   - Sets are mutable.
   - Example: `{1, 2, 3}`, `{'apple', 'banana'}`

Short Script Demonstrating Different Data Types

```python
# Integer
age = 25
print("Age:", age, "Type:", type(age))

# Floating-Point
height = 5.9
print("Height:", height, "Type:", type(height))

# String
name = "Alice"
print("Name:", name, "Type:", type(name))

# Boolean
is_student = True
print("Is Student:", is_student, "Type:", type(is_student))

# List
fruits = ["apple", "banana", "cherry"]
print("Fruits:", fruits, "Type:", type(fruits))

# Tuple
coordinates = (10.0, 20.0)
print("Coordinates:", coordinates, "Type:", type(coordinates))

# Dictionary
person = {"name": "Bob", "age": 30}
print("Person:", person, "Type:", type(person))

# Set
unique_numbers = {1, 2, 3, 4}
print("Unique Numbers:", unique_numbers, "Type:", type(unique_numbers))
```

Explanation

1. **Integer (`int`)**:
   - `age = 25` assigns an integer value to the variable `age`.

2. **Floating-Point (`float`)**:
   - `height = 5.9` assigns a floating-point value to the variable `height`.

3. **String (`str`)**:
   - `name = "Alice"` assigns a string value to the variable `name`.

4. **Boolean (`bool`)**:
   - `is_student = True` assigns a boolean value to the variable `is_student`.

5. **List (`list`)**:
   - `fruits = ["apple", "banana", "cherry"]` assigns a list of strings to the variable `fruits`.

6. **Tuple (`tuple`)**:
   - `coordinates = (10.0, 20.0)` assigns a tuple of floating-point numbers to the variable `coordinates`.

7. **Dictionary (`dict`)**:
   - `person = {"name": "Bob", "age": 30}` assigns a dictionary with keys and values to the variable `person`.

8. **Set (`set`)**:
   - `unique_numbers = {1, 2, 3, 4}` assigns a set of unique integers to the variable `unique_numbers`.

In this script, each variable is created with a specific data type, and the `type()` function is used to display the type of each variable, showing how Python handles different kinds of data.


5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.

   Conditional Statements

Conditional statements in Python allow you to execute code based on certain conditions. The primary conditional statement in Python is the `if-else` statement, which helps in decision-making.

`if-else` Statement

The `if-else` statement evaluates a condition and executes a block of code if the condition is `True`. You can also include `elif` (short for "else if") to check multiple conditions.

Syntax:

```python
if condition:
    # Code to execute if condition is True
elif another_condition:
    # Code to execute if another_condition is True
else:
    # Code to execute if none of the above conditions are True
```

Example:

```python
# Example of if-else statement
temperature = 30

if temperature > 25:
    print("It's hot outside.")
elif temperature == 25:
    print("The temperature is 25 degrees.")
else:
    print("It's cool outside.")
```

Explanation:

- `temperature > 25`: This condition checks if the temperature is greater than 25. If `True`, it prints "It's hot outside."
- `temperature == 25`: If the first condition is `False` but the temperature is exactly 25, it prints "The temperature is 25 degrees."
- The `else` block handles all other cases, printing "It's cool outside."

Loops

Loops are used to execute a block of code multiple times. The two primary types of loops in Python are `for` loops and `while` loops.

`for` Loop

The `for` loop is used to iterate over a sequence (such as a list, tuple, string, or range) and execute the code block for each item in the sequence.

Syntax:

```python
for variable in sequence:
    # Code to execute for each item in the sequence
```

Example:

```python
# Example of for loop
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Explanation:

- `for fruit in fruits`: This loop iterates over each item in the `fruits` list.
- `print(fruit)`: Prints each fruit in the list. The loop will execute this line for each item in the list, resulting in the output:
  ```
  apple
  banana
  cherry
  ```

Putting It All Together

Here's a combined example that includes both an `if-else` statement and a `for` loop:

```python
# Example combining if-else and for loop
numbers = [1, 2, 3, 4, 5]

for number in numbers:
    if number % 2 == 0:
        print(number, "is even.")
    else:
        print(number, "is odd.")
```

Explanation:

- The `for` loop iterates through each number in the `numbers` list.
- Inside the loop, the `if` statement checks if the number is even by using the modulus operator `%`.
- If `number % 2 == 0` evaluates to `True`, it prints that the number is even.
- If the condition is `False`, the `else` block prints that the number is odd.

Output:

```
1 is odd.
2 is even.
3 is odd.
4 is even.
5 is odd.
```

These control structures—`if-else` statements and loops—allow you to create programs that can handle a wide range of conditions and repetitive tasks.

6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.

   Functions in Python

**Functions** in Python are blocks of reusable code that perform a specific task. They help in organizing and managing code by encapsulating repetitive tasks into a single, callable unit. Functions improve code readability, reusability, and maintainability by allowing you to write a piece of code once and reuse it as needed.

Why Functions are Useful

1. **Reusability**: Write code once and reuse it multiple times.
2. **Modularity**: Break down complex problems into smaller, manageable pieces.
3. **Readability**: Improve the clarity of the code by naming functions descriptively.
4. **Maintainability**: Make code easier to update or debug by isolating functionality.

Defining and Using Functions

Here’s how you can define a simple function in Python that takes two arguments and returns their sum:

Function Definition:

```python
def add_numbers(a, b):
    """This function takes two arguments and returns their sum."""
    return a + b
```

Explanation:

- `def` is the keyword used to define a function.
- `add_numbers` is the name of the function.
- `(a, b)` are parameters (placeholders for the values the function will receive).
- `return` specifies the value to be returned by the function.
- The triple quotes `""" """` are used for a docstring, which describes what the function does (optional but useful for documentation).

Calling the Function:

To use the function, you need to call it with actual arguments:

```python
# Example of calling the function
result = add_numbers(5, 7)
print("The sum is:", result)
```

Explanation:

- `add_numbers(5, 7)` calls the function with `5` and `7` as arguments.
- The function returns the sum of these arguments (`12`).
- `result` stores the returned value.
- `print("The sum is:", result)` prints the result to the console.

Complete Example:

```python
def add_numbers(a, b):
    """This function takes two arguments and returns their sum."""
    return a + b

# Call the function
result = add_numbers(5, 7)
print("The sum is:", result)
```

Output:

```
The sum is: 12
```

Additional Details

- **Parameters vs. Arguments**: Parameters are variables listed as part of the function definition. Arguments are the actual values you pass to the function when calling it.
- **Default Parameters**: You can provide default values for parameters.
- **Keyword Arguments**: You can specify arguments by name when calling the function.
- **Variable-Length Arguments**: Functions can accept an arbitrary number of arguments using `*args` and `**kwargs`.

Here’s a quick example with default parameters:

```python
def greet(name="Guest"):
    """This function greets a person by name."""
    print(f"Hello, {name}!")

greet()         # Uses default parameter
greet("Alice")  # Uses provided argument
```

Output:

```
Hello, Guest!
Hello, Alice!
```

Functions are fundamental to writing organized, modular, and maintainable code in Python.

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.
   Differences Between Lists and Dictionaries

**Lists** and **dictionaries** are both versatile data structures in Python, but they serve different purposes and have different characteristics:

Lists

- **Ordered**: Lists maintain the order of elements based on their insertion sequence.
- **Indexed**: Elements in a list are accessed by their position (index), which starts from `0`.
- **Mutable**: Lists can be modified after creation (e.g., elements can be added, removed, or changed).
- **Homogeneous**: Lists can hold elements of different data types (though they are typically homogeneous).

Example: `numbers = [1, 2, 3, 4, 5]`

Dictionaries

- **Unordered**: Dictionaries do not maintain any order of elements; they are based on key-value pairs.
- **Key-Indexed**: Elements in a dictionary are accessed by keys, which must be unique and immutable (e.g., strings, numbers).
- **Mutable**: Dictionaries can be modified after creation (e.g., key-value pairs can be added, removed, or changed).
- **Flexible Keys**: Dictionary keys can be of any immutable data type, whereas values can be of any data type.

Example: `person = {"name": "Alice", "age": 30, "city": "New York"}`

Script Demonstrating Basic Operations

Here’s a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both:

```python
# Creating and operating on a list
numbers = [1, 2, 3, 4, 5]

print("List of numbers:", numbers)

# Adding an element to the list
numbers.append(6)
print("After appending 6:", numbers)

# Removing an element from the list
numbers.remove(3)
print("After removing 3:", numbers)

# Accessing an element by index
print("Element at index 2:", numbers[2])

# Iterating through the list
print("Iterating through the list:")
for number in numbers:
    print(number)

# Creating and operating on a dictionary
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

print("\nDictionary with key-value pairs:", person)

# Adding a new key-value pair
person["email"] = "alice@example.com"
print("After adding email:", person)

# Removing a key-value pair
del person["city"]
print("After removing city:", person)

# Accessing a value by key
print("Name:", person["name"])

# Iterating through the dictionary
print("Iterating through the dictionary:")
for key, value in person.items():
    print(f"{key}: {value}")
```

Explanation

List Operations:

1. Creation:
   ```python
   numbers = [1, 2, 3, 4, 5]
   ```

2. Appending:
   ```python
   numbers.append(6)
   ```
   Adds the number `6` to the end of the list.

3. Removing:
   ```python
   numbers.remove(3)
   ```
   Removes the first occurrence of `3` from the list.

4. Accessing by Index:
   ```python
   numbers[2]
   ```
   Accesses the element at index `2`, which is `3`.

5. Iterating:
   ```python
   for number in numbers:
       print(number)
   ```
   Iterates through each number in the list and prints it.

Dictionary Operations:

1. **Creation**:
   ```python
   person = {"name": "Alice", "age": 30, "city": "New York"}
   ```

2. **Adding Key-Value Pair**:
   ```python
   person["email"] = "alice@example.com"
   ```
   Adds a new key-value pair with key `"email"` and value `"alice@example.com"`.

3. **Removing Key-Value Pair**:
   ```python
   del person["city"]
   ```
   Removes the key-value pair with key `"city"`.

4. **Accessing by Key**:
   ```python
   person["name"]
   ```
   Retrieves the value associated with the key `"name"`.

5. **Iterating**:
   ```python
   for key, value in person.items():
       print(f"{key}: {value}")
   ```
   Iterates through each key-value pair in the dictionary and prints them.

Summary

- **Lists** are used for ordered collections of items that you can index and iterate through.
- **Dictionaries** are used for collections of key-value pairs, providing fast lookups and flexible data management.

These data structures are fundamental in Python and are widely used in various applications.

8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

Exception Handling in Python

**Exception handling** in Python is a mechanism to manage runtime errors or exceptional conditions that occur during program execution. It allows you to handle errors gracefully without crashing the program, providing a way to execute specific code in response to an error and clean up resources if necessary.

Key Components

1. **`try` Block**: Contains the code that might raise an exception.
2. **`except` Block**: Contains the code that handles the exception. You can have multiple `except` blocks to handle different types of exceptions.
3. **`finally` Block**: Contains the code that is always executed, regardless of whether an exception was raised or not. This is typically used for cleanup actions.

Example

Here’s an example of how to use `try`, `except`, and `finally` blocks in Python:

```python
try:
    # Code that may cause an exception
    numerator = 10
    denominator = int(input("Enter a number to divide 10 by: "))
    result = numerator / denominator
    print("Result:", result)

except ZeroDivisionError:
    # Handle division by zero error
    print("Error: Cannot divide by zero.")

except ValueError:
    # Handle invalid input (non-integer input)
    print("Error: Invalid input. Please enter a numeric value.")

finally:
    # Code that will always be executed
    print("Execution completed. Thank you for using the division program.")
```

Explanation

1. **`try` Block**:
   - The `try` block contains code that might raise exceptions. In this example, it attempts to divide `10` by a user-provided number.

2. **`except` Blocks**:
   - **`ZeroDivisionError`**: This block handles the case where the user tries to divide by zero. If the `denominator` is `0`, a `ZeroDivisionError` is raised, and the corresponding message is printed.
   - **`ValueError`**: This block handles invalid input where the user might enter a non-numeric value, resulting in a `ValueError`. The corresponding message informs the user about the invalid input.

3. **`finally` Block**:
   - This block executes regardless of whether an exception occurred or not. It prints a message indicating that the execution has been completed and thanks the user.

Additional Notes

- **Catching Multiple Exceptions**: You can catch multiple exceptions by specifying multiple `except` blocks, as shown in the example.
- **Exception Hierarchy**: You can also catch a general `Exception` if you want to handle any type of exception. However, it’s generally better to catch specific exceptions to handle known error conditions.
  
Example of Catching All Exceptions:

```python
try:
    # Code that may cause an exception
    numerator = 10
    denominator = int(input("Enter a number to divide 10 by: "))
    result = numerator / denominator
    print("Result:", result)

except Exception as e:
    # Handle any exception
    print("An error occurred:", str(e))

finally:
    print("Execution completed. Thank you for using the division program.")
```

In this example, `Exception as e` captures any exception and `str(e)` provides a description of the error.

Exception handling is essential for building robust programs that can gracefully handle unexpected situations and errors.



9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.

   In Python, **modules** and **packages** are essential concepts for organizing and reusing code.

 Modules

A **module** is a single file that contains Python definitions and statements. This file can define functions, classes, and variables that you can use in other Python scripts. Modules help you organize your code logically.

How to Create a Module

You create a module by simply writing Python code in a file with a `.py` extension. For example, if you have a file named `mymodule.py` with the following code:

```python
# mymodule.py
def greet(name):
    return f"Hello, {name}!"
```

Packages

A **package** is a collection of modules. It's a directory that contains multiple module files and an `__init__.py` file, which can be empty or include package initialization code. Packages allow you to organize modules hierarchically.

How to Create a Package

To create a package, you need to:
1. Create a directory for the package.
2. Place your module files in this directory.
3. Include an `__init__.py` file in the directory.

For example, if you have a directory structure like this:

```
mypackage/
    __init__.py
    module1.py
    module2.py
```

The `__init__.py` file can be empty, but it indicates that `mypackage` is a package.

Importing and Using Modules

You can import a module using the `import` statement. Here’s how you can use the built-in `math` module in your script:

 Example with `math` Module

The `math` module provides mathematical functions and constants. Here’s an example of how to use it:

```python
# Importing the entire math module
import math

# Using functions from the math module
radius = 5
area = math.pi * (radius ** 2)
print(f"The area of the circle with radius {radius} is {area:.2f}")

# Using a specific function from the math module
square_root = math.sqrt(25)
print(f"The square root of 25 is {square_root}")
```

In this example:
- `import math` imports the entire `math` module.
- `math.pi` accesses the value of π.
- `math.sqrt` calculates the square root of a number.

By using modules and packages, you can keep your code well-organized and reusable.


10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.

    In Python, file I/O (Input/Output) operations are straightforward. You can use the built-in `open()` function to read from and write to files. 

Reading from a File

To read from a file, you open it in read mode (`'r'`), use the `read()` or `readlines()` method to get its content, and then close the file.

Here’s a script that reads the content of a file and prints it to the console:

```python
# Script to read from a file and print its content
filename = 'example.txt'

# Open the file in read mode
with open(filename, 'r') as file:
    # Read the entire content of the file
    content = file.read()
    # Print the content to the console
    print(content)
```

In this script:
- `with open(filename, 'r') as file:` opens the file and ensures it’s properly closed after the block of code is executed.
- `file.read()` reads the entire file content.
- The file is automatically closed when the `with` block is exited.

Writing to a File

To write to a file, you open it in write mode (`'w'`), append mode (`'a'`), or another appropriate mode. The `write()` method allows you to write strings to the file. 

Here’s a script that writes a list of strings to a file:

```python
# Script to write a list of strings to a file
filename = 'output.txt'
lines = [
    'First line of the file.',
    'Second line of the file.',
    'Third line of the file.'
]

# Open the file in write mode
with open(filename, 'w') as file:
    # Write each line from the list to the file
    for line in lines:
        file.write(line + '\n')  # Add a newline character after each line
```

In this script:
- `with open(filename, 'w') as file:` opens the file in write mode. If the file already exists, its content is overwritten.
- `file.write(line + '\n')` writes each string from the list to the file, appending a newline character after each line to ensure they are separated properly.

By using these techniques, you can efficiently handle file input and output in your Python programs.

# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


