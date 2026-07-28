# Input & Output

Input allows a program to receive data from the user.

Output allows a program to display information to the user.

---

# print() Function

The `print()` function displays output on the screen.

```python
print("Hello, World!")
```

Output

```
Hello, World!
```

Printing numbers:

```python
print(100)
print(3.14)
```

Output

```
100
3.14
```

Printing variables:

```python
name = "Vinay"
age = 20

print(name)
print(age)
```

Output

```
Vinay
20
```

Printing multiple values:

```python
name = "Vinay"
age = 20

print(name, age)
```

Output

```
Vinay 20
```

---

# sep Parameter

The `sep` parameter changes the separator between values.

```python
print("Python", "Java", "C++", sep=" | ")
```

Output

```
Python | Java | C++
```

Example

```python
print(2026, 7, 28, sep="-")
```

Output

```
2026-7-28
```

---

# end Parameter

The `end` parameter changes what is printed after the output.

Default value is `\n` (new line).

```python
print("Hello", end=" ")
print("World")
```

Output

```
Hello World
```

---

# Escape Characters

## New Line (`\n`)

```python
print("Hello\nWorld")
```

Output

```
Hello
World
```

---

## Tab (`\t`)

```python
print("Name\tAge")
```

Output

```
Name    Age
```

---

## Backslash (`\\`)

```python
print("C:\\Users\\Kumar")
```

Output

```
C:\Users\Kumar
```

---

## Double Quote (`\"`)

```python
print("She said \"Hello\"")
```

Output

```
She said "Hello"
```

---

## Single Quote (`\'`)

```python
print('It\'s Python')
```

Output

```
It's Python
```

---

# Multi-line String

Use triple quotes for multiple lines.

```python
text = """
Python
Java
C++
"""

print(text)
```

Output

```
Python
Java
C++
```

---

# input() Function

The `input()` function reads data from the keyboard.

```python
name = input("Enter your name: ")

print(name)
```

Output

```
Enter your name: Kumar
Kumar
```

---

# input() Always Returns a String

```python
age = input("Enter age: ")

print(type(age))
```

Output

```
<class 'str'>
```

Even if the user enters a number, Python stores it as a string.

---

# Integer Input

Convert using `int()`.

```python
age = int(input("Enter age: "))

print(age)
print(type(age))
```

Output

```
20
<class 'int'>
```

---

# Float Input

```python
price = float(input("Enter price: "))

print(price)
```

Output

```
99.99
```

---

# Boolean Input

```python
value = bool(input("Enter something: "))

print(value)
```

Output (User enters Hello)

```
True
```

Output (User presses Enter)

```
False
```

---

# Multiple Inputs

```python
name = input("Name: ")
age = int(input("Age: "))

print(name, age)
```

Output

```
Name: Kumar
Age: 20
Kumar 20
```

---

# Multiple Inputs in One Line

```python
name, age = input("Enter name and age: ").split()

print(name)
print(age)
```

Input

```
Kumar 20
```

Output

```
Kumar
20
```

---

# Using map()

```python
a, b = map(int, input("Enter two numbers: ").split())

print(a + b)
```

Input

```
10 20
```

Output

```
30
```

---

# List Input

```python
numbers = list(map(int, input().split()))

print(numbers)
```

Input

```
10 20 30 40
```

Output

```
[10, 20, 30, 40]
```

---

# String Formatting

## Concatenation

```python
name = "Vinay"

print("Hello " + name)
```

Output

```
Hello Vinay
```

---

# f-Strings (Recommended)

```python
name = "Vinay"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

Output

```
My name is Vinay and I am 20 years old.
```

---

# format() Method

```python
name = "Vinay"
age = 20

print("My name is {} and I am {}.".format(name, age))
```

Output

```
My name is Vinay and I am 20.
```

---

# Old % Formatting

```python
name = "Vinay"

print("Hello %s" % name)
```

Output

```
Hello Vinay
```

---

# Common Beginner Mistakes

## Forgetting Type Conversion

Wrong

```python
age = input("Age: ")

print(age + 10)
```

Error

```
TypeError
```

Correct

```python
age = int(input("Age: "))

print(age + 10)
```

---

## Missing split()

Wrong

```python
a, b = input()
```

Correct

```python
a, b = input().split()
```

---

## Mixing String and Integer

Wrong

```python
print("Age: " + 20)
```

Correct

```python
print("Age:", 20)
```

or

```python
print("Age: " + str(20))
```

---

# Best Practices

- Always use meaningful prompts.
- Convert input to the required data type immediately.
- Prefer f-strings for output formatting.
- Validate user input when necessary.
- Use `map()` for multiple numeric inputs.

---

# Quick Summary

You learned:

- `print()`
- `sep`
- `end`
- Escape Characters
- `input()`
- Type Conversion
- Multiple Inputs
- `split()`
- `map()`
- List Input
- f-Strings
- `format()`
- Common Mistakes
- Best Practices

You can now take input from users, display formatted output, and build interactive Python programs.

---

# Next Topic

➡️ Control Flow (if, elif, else)