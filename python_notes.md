# Python Handbook Notes

## 1. Introduction to Python
- **What is Programming?**: Writing instructions for computers using code.
- **Why Python?**:
  - Simple, readable, high-level, interpreted language.
  - Used in web development (Django, Flask), data science (Pandas, NumPy), automation, and game development (Pygame).
  - Beginner-friendly with a large community and extensive libraries.

## 2. Setting Up Python
- **Installation**:
  - Download from python.org.
  - Check "Add Python to PATH" during installation.
  - Verify: `python --version` (e.g., Python 3.13.5).
- **IDEs**:
  - VS Code: Lightweight, customizable.
  - PyCharm: Advanced, professional.
  - Jupyter Notebook: Great for data science.
  - IDLE: Basic, pre-installed with Python.

## 3. First Program
- **Hello, World!**:
  ```python
  print("Hello, World!")  # Save as hello.py, run with `python hello.py`
  ```
- **Key**: `print()` displays output; Python executes code line by line.

## 4. Python Syntax
- **Indentation**: Defines code blocks (use 4 spaces).
  ```python
  if 5 > 2:
      print("Five is greater than two!")
  ```
- **Whitespace**: Consistent indentation is critical.
- **Comments**:
  - Single-line: `# Comment`
  - Multi-line: `"""Comment"""` or `'''Comment'''`

## 5. Variables and Data Types
- **Variables**: Store data using `=`.
  ```python
  name = "Alice"  # String
  age = 25        # Integer
  height = 5.6    # Float
  ```
- **Naming Rules**:
  - Letters, numbers, underscores; start with letter or underscore.
  - Case-sensitive; avoid Python keywords (e.g., `print`, `if`).
- **Best Practices**: Use descriptive, lowercase names with underscores (e.g., `first_name`).
- **Data Types**:
  - `int`: Whole numbers (10, -5).
  - `float`: Decimals (3.14, -0.001).
  - `str`: Text ("Hello").
  - `bool`: True/False.
  - `list`: Ordered, mutable `[1, 2, 3]`.
  - `tuple`: Ordered, immutable `(1, 2, 3)`.
  - `set`: Unordered, unique `{1, 2, 3}`.
  - `dict`: Key-value pairs `{"name": "Alice", "age": 25}`.
- **Typechecking**: `type(10)` → `<class 'int'>`.
- **Typecasting**:
  ```python
  num_str = "10"
  num_int = int(num_str)  # Convert to integer
  ```

## 6. User Input
- **input()**: Takes user input as a string.
  ```python
  name = input("Enter your name: ")
  age = int(input("Enter your age: "))
  print(f"Hello {name}, you are {age} years old.")
  ```

## 7. Strings
- **Creating**:
  ```python
  a = 'Hello'  # Single quotes
  b = "World"  # Double quotes
  c = """Multi-line"""  # Triple quotes
  ```
- **Indexing**: `text = "Python"; text[0]` → `P`; `text[-1]` → `n`.
- **Slicing**: `text[0:5]` → `Hello`; `text[::-1]` reverses string.
- **Methods**:
  - `upper()`, `lower()`, `title()`, `capitalize()`.
  - `strip()`, `lstrip()`, `rstrip()`: Remove whitespace.
  - `find()`, `replace()`, `split()`, `join()`.
- **Formatting**:
  - `.format()`: `"My name is {}".format("Alice")`.
  - **f-strings** (Python 3.6+): `f"My name is {name}"`.

## 8. Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`, `**` (exponent), `//` (floor division).
- **Comparison**: `==`, `!=`, `>`, `<`, `>=`, `<=`.
- **Logical**: `and`, `or`, `not`.
- **Assignment**: `=`, `+=`, `-=`, etc.
- **Membership**: `in`, `not in`.
- **Identity**: `is`, `is not`.

## 9. Control Flow
- **If-Else**:
  ```python
  age = 18
  if age < 18:
      print("Minor")
  elif age == 18:
      print("Just adult")
  else:
      print("Adult")
  ```
- **Match-Case** (Python 3.10+):
  ```python
  status = 404
  match status:
      case 200: print("Success!")
      case 404: print("Not Found")
      case _: print("Unknown")
  ```
- **Loops**:
  - **For**: Iterate over sequences.
    ```python
    for fruit in ["apple", "banana"]: print(fruit)
    for i in range(5): print(i)  # 0 to 4
    ```
  - **While**: Run while condition is True.
    ```python
    count = 0
    while count < 5:
        print(count)
        count += 1
    ```
- **Control**: `break` (exit loop), `continue` (skip iteration), `pass` (do nothing).

## 10. Functions
- **Defining**:
  ```python
  def greet(name):
      return f"Hello, {name}!"
  print(greet("Alice"))  # Hello, Alice!
  ```
- **Arguments**:
  - Positional: `def add(a, b): return a + b`.
  - Default: `def greet(name="Guest"): return f"Hello, {name}!"`.
  - Keyword: `student(age=20, name="Bob")`.
  - `*args`: Variable positional arguments (tuple).
  - `**kwargs`: Variable keyword arguments (dict).
    ```python
    def func(*args, **kwargs):
        print(args, kwargs)
    func(1, 2, x=3, y=4)  # (1, 2) {'x': 3, 'y': 4}
    ```
- **Lambda**: `square = lambda x: x * x; print(square(4))` → `16`.
- **Recursion**:
  ```python
  def factorial(n):
      if n == 1: return 1
      return n * factorial(n-1)
  print(factorial(5))  # 120
  ```
- **Docstrings**:
  ```python
  def add(a, b):
      """Returns sum of two numbers."""
      return a + b
  print(add.__doc__)  # Returns sum of two numbers.
  ```

## 11. Data Structures
- **Lists**: Ordered, mutable.
  ```python
  my_list = [1, 2, 3]
  my_list.append(4)  # Add item
  my_list.sort()     # Sort list
  ```
  - **Comprehensions**: `[x**2 for x in range(5)]` → `[0, 1, 4, 9, 16]`.
- **Tuples**: Ordered, immutable.
  ```python
  my_tuple = (1, 2, 3)
  a, b, c = my_tuple  # Unpacking
  ```
- **Sets**: Unordered, unique.
  ```python
  my_set = {1, 2, 3}
  my_set.add(4)  # Add item
  ```
- **Dictionaries**: Key-value pairs.
  ```python
  student = {"name": "Alice", "age": 21}
  print(student["name"])  # Alice
  ```

## 12. Object-Oriented Programming (OOP)
- **Principles**:
  - **Abstraction**: Hide complex details.
  - **Encapsulation**: Bundle data and methods.
  - **Inheritance**: Reuse code via parent-child classes.
  - **Polymorphism**: Same method, different behaviors.
- **Classes and Objects**:
  ```python
  class Dog:
      species = "Canis familiaris"  # Class attribute
      def __init__(self, name, breed):
          self.name = name  # Instance attribute
          self.breed = breed
      def bark(self):
          print(f"{self.name} says Woof!")
  my_dog = Dog("Buddy", "Golden Retriever")
  my_dog.bark()  # Buddy says Woof!
  ```
- **Inheritance**:
  ```python
  class Animal:
      def __init__(self, name):
          self.name = name
      def speak(self):
          print("Generic sound")
  class Dog(Animal):
      def speak(self):
          print("Woof!")
  ```
- **Magic Methods**:
  ```python
  class Point:
      def __init__(self, x, y):
          self.x = x
          self.y = y
      def __add__(self, other):
          return Point(self.x + other.x, self.y + other.y)
      def __str__(self):
          return f"({self.x}, {self.y})"
  p1 = Point(1, 2)
  p2 = Point(3, 4)
  print(p1 + p2)  # (4, 6)
  ```
- **Getters/Setters**:
  ```python
  class Person:
      def __init__(self, name):
          self._name = name
      @property
      def name(self):
          return self._name
      @name.setter
      def name(self, new_name):
          self._name = new_name
  p = Person("Alice")
  p.name = "Bob"  # Sets name
  print(p.name)   # Bob
  ```

## 13. Exception Handling
- **Try-Except**:
  ```python
  try:
      x = 10 / 0
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  else:
      print("No errors")
  finally:
      print("Always runs")
  ```
- **Custom Exceptions**:
  ```python
  class InvalidAgeError(Exception):
      pass
  def verify_age(age):
      if age < 18:
          raise InvalidAgeError("Age must be 18+")
  ```

## 14. Map, Filter, Reduce
- **Map**: Apply function to each item.
  ```python
  numbers = [1, 2, 3]
  squared = list(map(lambda x: x**2, numbers))  # [1, 4, 9]
  ```
- **Filter**: Keep items where function returns True.
  ```python
  even = list(filter(lambda x: x % 2 == 0, numbers))  # [2]
  ```
- **Reduce**: Aggregate items to a single value.
  ```python
  from functools import reduce
  sum = reduce(lambda x, y: x + y, numbers)  # 6
  ```

## 15. Walrus Operator (:=) (Python 3.8+)
- Assigns and uses a value in one expression.
  ```python
  while (data := input("Enter value: ")) != "quit":
      print(f"You entered: {data}")
  ```

## 16. File Handling
- **Read/Write**:
  ```python
  with open("file.txt", "r") as file:
      content = file.read()
  with open("file.txt", "w") as file:
      file.write("Hello")
  ```
- **OS Module**:
  ```python
  import os
  print(os.getcwd())  # Current directory
  os.mkdir("new_folder")
  ```

## 17. External Libraries
- **Virtual Environments**:
  ```bash
  python3 -m venv my_env
  source my_env/bin/activate  # macOS/Linux
  pip install requests
  ```
- **Requests**: HTTP requests.
  ```python
  import requests
  response = requests.get("https://api.github.com")
  print(response.json())
  ```
- **Regex (re)**:
  ```python
  import re
  text = "Hello world"
  matches = re.findall("world", text)  # ['world']
  ```

## 18. Multithreading
- For I/O-bound tasks.
  ```python
  import threading
  def worker(num):
      print(f"Thread {num}: Starting")
  threads = [threading.Thread(target=worker, args=(i,)) for i in range(3)]
  for t in threads: t.start()
  for t in threads: t.join()
  ```

## 19. Key Takeaways
- Python is versatile, beginner-friendly, and widely used.
- Focus on indentation, clear variable names, and modular code.
- Use OOP for structured, reusable code.
- Handle errors gracefully with try-except.
- Leverage libraries and virtual environments for efficient development.
