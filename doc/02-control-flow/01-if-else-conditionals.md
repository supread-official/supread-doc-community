# If-Else in Python

> Make decisions in your program based on conditions.

---

# What is If-Else?

`if`, `elif`, and `else` are used to execute different blocks of code depending on whether a condition is `True` or `False`.

```python
age = 18

if age >= 18:
    print("You can vote")
```

**Output**

```
You can vote
```

---

# Syntax

```python
if condition:
    # Code to execute if condition is True
```

Example:

```python
temperature = 35

if temperature > 30:
    print("It's hot")
```

---

# Indentation

Python uses **indentation (spaces)** instead of braces `{}`.

✅ Correct

```python
age = 20

if age >= 18:
    print("Adult")
```

❌ Wrong

```python
age = 20

if age >= 18:
print("Adult")
```

This will produce:

```
IndentationError
```

---

# if Statement

Runs only when the condition is `True`.

```python
number = 10

if number > 0:
    print("Positive number")
```

Output

```
Positive number
```

---

# if-else Statement

Executes one block if the condition is `True`, otherwise executes another.

```python
age = 15

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

Output

```
Minor
```

---

# if-elif-else Statement

Used when there are multiple conditions.

```python
marks = 82

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 60:
    print("Grade C")
else:
    print("Fail")
```

Output

```
Grade B
```

---

# Multiple elif

You can use as many `elif` blocks as needed.

```python
day = 5

if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday")
elif day == 4:
    print("Thursday")
elif day == 5:
    print("Friday")
else:
    print("Weekend")
```

---

# Nested if

An `if` inside another `if`.

```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("You can drive")
```

Output

```
You can drive
```

---

# Comparison Operators

| Operator | Meaning | Example |
|----------|---------|---------|
| `==` | Equal | `a == b` |
| `!=` | Not Equal | `a != b` |
| `>` | Greater Than | `a > b` |
| `<` | Less Than | `a < b` |
| `>=` | Greater or Equal | `a >= b` |
| `<=` | Less or Equal | `a <= b` |

Example

```python
x = 20

if x >= 10:
    print("Greater than or equal to 10")
```

---

# Logical Operators with if

## and

Both conditions must be `True`.

```python
age = 22
citizen = True

if age >= 18 and citizen:
    print("Eligible to vote")
```

---

## or

At least one condition must be `True`.

```python
day = "Sunday"

if day == "Saturday" or day == "Sunday":
    print("Weekend")
```

---

## not

Reverses the condition.

```python
logged_in = False

if not logged_in:
    print("Please login")
```

---

# Boolean Values

```python
is_admin = True

if is_admin:
    print("Access granted")
```

---

# Truthy and Falsy Values

Python treats some values as `False`.

Falsy values

```python
False
0
0.0
''
""
[]
{}
set()
None
```

Everything else is generally considered `True`.

Example

```python
name = ""

if name:
    print("Name exists")
else:
    print("Name is empty")
```

Output

```
Name is empty
```

---

# Checking Multiple Conditions

```python
number = 15

if number > 0 and number % 3 == 0:
    print("Positive and divisible by 3")
```

---

# Membership with if

Using `in`

```python
fruits = ["Apple", "Banana", "Mango"]

if "Mango" in fruits:
    print("Found")
```

Output

```
Found
```

---

# Identity with if

Using `is`

```python
a = None

if a is None:
    print("No value")
```

---

# One-Line if

```python
age = 20

if age >= 18:
    print("Adult")
```

---

# One-Line if-else (Ternary Operator)

Syntax

```python
value_if_true if condition else value_if_false
```

Example

```python
age = 16

status = "Adult" if age >= 18 else "Minor"

print(status)
```

Output

```
Minor
```

---

# Pass Statement

Use `pass` when you don't want to write code yet.

```python
age = 20

if age >= 18:
    pass
```

---

# Practical Examples

## Check Even or Odd

```python
number = 8

if number % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

## Positive, Negative or Zero

```python
number = -5

if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

---

## Largest of Two Numbers

```python
a = 15
b = 22

if a > b:
    print(a)
else:
    print(b)
```

---

## Password Check

```python
password = "python123"

if password == "python123":
    print("Access Granted")
else:
    print("Wrong Password")
```

---

## Login Example

```python
username = "admin"
password = "1234"

if username == "admin" and password == "1234":
    print("Login Successful")
else:
    print("Invalid Credentials")
```

---

## Grade Calculator

```python
marks = 91

if marks >= 90:
    grade = "A"
elif marks >= 80:
    grade = "B"
elif marks >= 70:
    grade = "C"
elif marks >= 60:
    grade = "D"
else:
    grade = "F"

print(grade)
```

---

# Common Beginner Mistakes

## 1. Using `=` instead of `==`

❌ Wrong

```python
if age = 18:
    print("Adult")
```

✅ Correct

```python
if age == 18:
    print("Adult")
```

---

## 2. Wrong Indentation

❌

```python
if True:
print("Hello")
```

✅

```python
if True:
    print("Hello")
```

---

## 3. Forgetting the Colon

❌

```python
if age > 18
    print("Adult")
```

✅

```python
if age > 18:
    print("Adult")
```

---

## 4. Incorrect Order

❌

```python
else:
    print("Other")

elif x == 5:
    print(x)
```

✅

```python
if x == 1:
    print(x)
elif x == 5:
    print(x)
else:
    print("Other")
```

---

# Interview Questions

### What is the difference between `if`, `elif`, and `else`?

- `if` checks the first condition.
- `elif` checks additional conditions.
- `else` runs when no previous condition is `True`.

---

### Can we have multiple `if` statements?

Yes.

```python
x = 10

if x > 5:
    print("Greater than 5")

if x > 8:
    print("Greater than 8")
```

---

### Is `else` mandatory?

No.

```python
age = 20

if age >= 18:
    print("Adult")
```

---

### Can `elif` exist without `if`?

No.

---

### Can we use multiple `else` blocks?

No.

---

# Quick Summary

- `if` executes code when a condition is `True`.
- `else` executes when the condition is `False`.
- `elif` checks additional conditions.
- Python uses indentation instead of braces.
- Conditions can use comparison, logical, membership, and identity operators.
- Nested `if` statements allow more complex decision-making.
- The ternary operator provides a concise one-line `if-else`.
- `pass` acts as a placeholder for future code.

---

## What's Next?

The next topic is **Loops (`for` and `while`)**, where you'll learn how to execute code repeatedly without writing it multiple times.