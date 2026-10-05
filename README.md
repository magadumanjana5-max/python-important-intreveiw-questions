# Python Important Interview Questions

This README contains 20 important Python interview questions with short, practical answers that are useful for technical interviews.

---

## 1) What is Python?
**Answer:** Python is a high-level, interpreted, general-purpose programming language known for its simple syntax and readability. It is widely used in web development, data science, automation, AI, and scripting.

## 2) What are the key features of Python?
**Answer:** Some important features are:
- Easy to read and write
- Interpreted language
- Dynamically typed
- Object-oriented and functional support
- Large standard library
- Cross-platform compatibility

## 3) What is the difference between a list and a tuple in Python?
**Answer:**
- List is mutable; tuple is immutable.
- List syntax: `[1, 2, 3]`; tuple syntax: `(1, 2, 3)`.
- Lists are used when values may change; tuples are used for fixed data.

## 4) What is a Python dictionary?
**Answer:** A dictionary is an unordered collection of key-value pairs. Keys are unique and immutable, while values can be of any type. Example:
```python
student = {"name": "Alice", "age": 22}
```

## 5) What is the difference between deep copy and shallow copy?
**Answer:**
- Shallow copy copies the outer object but not nested objects.
- Deep copy recursively copies all nested objects.
- Deep copy is safer when nested structures are involved.

## 6) What is a lambda function in Python?
**Answer:** A lambda function is an anonymous function defined using the `lambda` keyword. It is used for short, simple operations.
```python
square = lambda x: x * x
print(square(5))
```

## 7) What is list comprehension?
**Answer:** List comprehension is a concise way to create lists from an existing iterable.
```python
squares = [x * x for x in range(1, 6)]
print(squares)
```

## 8) What are *args and **kwargs?
**Answer:**
- `*args` allows a function to accept any number of positional arguments.
- `**kwargs` allows a function to accept any number of keyword arguments.
```python
def demo(*args, **kwargs):
    print(args)
    print(kwargs)
```

## 9) What is a decorator in Python?
**Answer:** A decorator is a function that modifies or extends the behavior of another function without changing its source code. Example:
```python
def decorator(func):
    def wrapper():
        print("Before call")
        func()
        print("After call")
    return wrapper
```

## 10) What is the difference between iterator and iterable?
**Answer:**
- An iterable is an object that can be looped over, like a list or tuple.
- An iterator is an object used to iterate through an iterable using `next()`.
- Lists are iterables, and iterators are produced from them using `iter()`.

## 11) What is a generator in Python?
**Answer:** A generator is a function that returns an iterator and uses `yield` instead of `return`. Generators are memory efficient because they generate values one at a time.
```python
def fib():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b
```

## 12) What is Python's GIL (Global Interpreter Lock)?
**Answer:** GIL is a mutex in CPython that allows only one thread to execute Python bytecode at a time. It limits true multithreading in CPU-bound tasks, though I/O-bound tasks can still benefit from threading.

## 13) What is the difference between mutable and immutable objects?
**Answer:**
- Mutable objects can be changed after creation, like lists and dictionaries.
- Immutable objects cannot be changed after creation, like strings, tuples, and integers.
- Immutability helps with data safety and hashability.

## 14) What is PEP 8?
**Answer:** PEP 8 is the official style guide for Python code. It defines conventions for indentation, naming, line length, and readability. Following PEP 8 makes the code cleaner and easier to maintain.

## 15) What is exception handling in Python?
**Answer:** Python uses `try`, `except`, `else`, and `finally` blocks to handle exceptions gracefully.
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Division by zero")
finally:
    print("This always runs")
```

## 16) What is the difference between `==` and `is` in Python?
**Answer:**
- `==` compares values.
- `is` compares object identity (whether both variables refer to the same object).
```python
a = [1, 2]
b = [1, 2]
print(a == b)   # True
print(a is b)  # False
```

## 17) What is the difference between `append()` and `extend()` in lists?
**Answer:**
- `append()` adds a single element to the end of the list.
- `extend()` adds multiple elements from an iterable.
```python
lst = [1, 2]
lst.append(3)      # [1, 2, 3]
lst.extend([4, 5]) # [1, 2, 3, 4, 5]
```

## 18) What is the purpose of `__init__` in a class?
**Answer:** `__init__` is the constructor method in a class. It is called automatically when an object is created and is used to initialize instance variables.
```python
class Person:
    def __init__(self, name):
        self.name = name
```

## 19) What is method overloading in Python?
**Answer:** Python does not support method overloading in the same way as Java or C++. However, default arguments and variable-length arguments can be used to achieve similar behavior.

## 20) What is monkey patching in Python?
**Answer:** Monkey patching means modifying a class or module at runtime to change or extend its behavior. It is often used in testing and frameworks, but it should be used carefully because it can make code harder to understand.

---

## Final Tips
To prepare for a Python interview, practice:
- Core syntax and data structures
- OOP concepts
- Exception handling
- Functional programming basics
- File handling and modules
- Multi-threading and memory management

These concepts are commonly asked in Python interviews and help build a strong foundation.
