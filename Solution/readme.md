### **Exercises**

#### **Exercise 1: Calculator with Error Handling**

**Objective:** Create a calculator program that handles division by zero and invalid input errors.

**Instructions:**

1. Prompt the user for two numbers and an operator (`+`, `-`, `*`, `/`).
2. Perform the calculation.
3. Use `try-except` blocks to handle exceptions.
4. Display appropriate error messages.

**Solution:**

```python
def calculator():
    try:
        num1 = float(input("Enter the first number: "))
        operator = input("Enter an operator (+, -, *, /): ")
        num2 = float(input("Enter the second number: "))

        if operator == '+':
            result = num1 + num2
        elif operator == '-':
            result = num1 - num2
        elif operator == '*':
            result = num1 * num2
        elif operator == '/':
            result = num1 / num2
        else:
            print("Invalid operator.")
            return

    except ZeroDivisionError:
        print("Error: Cannot divide by zero.")
    except ValueError:
        print("Error: Invalid input.")
    else:
        print(f"Result: {result}")

calculator()
```

---

#### **Exercise 2: Custom Module Creation**

**Objective:** Create a custom module `utilities.py` with helpful functions and use it in another script.

**Instructions:**

1. **In `utilities.py`**, define the following functions:
   - `is_even(number)`: Returns `True` if the number is even, else `False`.
   - `is_odd(number)`: Returns `True` if the number is odd, else `False`.
2. **In `main.py`**, import `utilities` and use the functions.
3. Prompt the user for a number and display whether it's even or odd.

**Solution (`utilities.py`):**

```python
# utilities.py

def is_even(number):
    return number % 2 == 0

def is_odd(number):
    return number % 2 != 0
```

**Solution (`main.py`):**

```python
# main.py

import utilities

num = int(input("Enter a number: "))

if utilities.is_even(num):
    print(f"{num} is even.")
else:
    print(f"{num} is odd.")
```

---
