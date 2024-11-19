### **Lecture Notes**

#### **1. Advanced Functions**

##### **Default Parameters**

Parameters can have default values.

**Example:**

```python
def greet(name, message="Hello"):
    print(f"{message}, {name}!")

greet("Alice")              # Uses default message
greet("Bob", "Welcome")     # Overrides default message
```

**Output:**

```
Hello, Alice!
Welcome, Bob!
```

##### **Keyword Arguments**

Specify arguments by parameter name.

**Example:**

```python
def calculate_area(width, height):
    return width * height

area = calculate_area(height=10, width=5)
print(area)
```

**Output:**

```
50
```

##### **Variable-Length Arguments**

- **`*args`**: Non-keyword variable-length arguments.
- **`**kwargs`**: Keyword variable-length arguments.

**Example with `*args`:**

```python
def add_numbers(*args):
    return sum(args)

print(add_numbers(1, 2, 3))         # Outputs: 6
print(add_numbers(4, 5, 6, 7, 8))   # Outputs: 30
```

**Example with `**kwargs`:**

```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25, city="New York")
```

**Output:**

```
name: Alice
age: 25
city: New York
```

##### **Lambda Functions**

Anonymous, inline functions.

**Syntax:**

```python
lambda arguments: expression
```

**Example:**

```python
multiply = lambda x, y: x * y
print(multiply(5, 3))
```

**Output:**

```
15
```

---

#### **2. Modules and Packages**

Modules are files containing Python definitions and statements. Packages are a way of structuring Python's module namespace by using dotted module names.

##### **Importing Modules**

```python
import math
from datetime import datetime
```

##### **Using Module Functions**

```python
print(math.pi)
print(datetime.now())
```

##### **Creating Custom Modules**

1. **Create a Python file (e.g., `mymodule.py`):**

```python
# mymodule.py

def greet(name):
    print(f"Hello, {name}!")
```

2. **Import and use the module:**

```python
import mymodule

mymodule.greet("Alice")
```

**Output:**

```
Hello, Alice!
```

---

#### **3. Error and Exception Handling**

Handling exceptions prevents your program from crashing due to unexpected errors.

##### **Syntax:**

```python
try:
    # code that may raise an exception
except ExceptionType:
    # code to handle the exception
else:
    # code that runs if no exception occurs
finally:
    # code that runs regardless of exceptions
```

##### **Example:**

```python
try:
    numerator = int(input("Enter numerator: "))
    denominator = int(input("Enter denominator: "))
    result = numerator / denominator
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
except ValueError:
    print("Error: Invalid input.")
else:
    print(f"Result: {result}")
finally:
    print("Execution completed.")
```

---
