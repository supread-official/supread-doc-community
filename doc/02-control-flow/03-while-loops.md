# While Loop in Python

> Execute a block of code repeatedly as long as a condition remains `True`.

---

# What is a While Loop?

A `while` loop repeatedly executes a block of code **until its condition becomes `False`**.

Unlike a `for` loop, which iterates over a sequence, a `while` loop depends on a **condition**.

Example

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Output

```
1
2
3
4
5
```

---

# Syntax

```python
while condition:
    # Code to execute
```

Example

```python
number = 1

while number <= 3:
    print("Hello")
    number += 1
```

Output

```
Hello
Hello
Hello
```

---

# How a While Loop Works

```python
x = 1

while x <= 3:
    print(x)
    x += 1
```

Flow

```
Start
   ↓
Check Condition
   ↓
True?
   ↓
Execute Code
   ↓
Update Variable
   ↓
Go Back to Condition
   ↓
False?
   ↓
Stop
```

---

# Basic Example

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

Output

```
1
2
3
4
5
```

---

# Countdown Example

```python
count = 5

while count > 0:
    print(count)
    count -= 1

print("Blast Off!")
```

Output

```
5
4
3
2
1
Blast Off!
```

---

# Infinite Loop

If the condition never becomes `False`, the loop runs forever.

```python
while True:
    print("Running...")
```

⚠️ Stop an infinite loop using **Ctrl + C** in the terminal.

---

# Avoid Infinite Loops

❌ Wrong

```python
count = 1

while count <= 5:
    print(count)
```

The value of `count` never changes.

✅ Correct

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

---

# break Statement

`break` immediately exits the loop.

```python
number = 1

while number <= 10:
    if number == 6:
        break

    print(number)
    number += 1
```

Output

```
1
2
3
4
5
```

---

# continue Statement

`continue` skips the current iteration.

```python
number = 0

while number < 5:
    number += 1

    if number == 3:
        continue

    print(number)
```

Output

```
1
2
4
5
```

---

# pass Statement

Use `pass` as a placeholder.

```python
while False:
    pass
```

---

# else with While Loop

The `else` block executes only if the loop ends normally.

```python
count = 1

while count <= 3:
    print(count)
    count += 1
else:
    print("Loop Finished")
```

Output

```
1
2
3
Loop Finished
```

Example with `break`

```python
count = 1

while count <= 5:
    if count == 3:
        break

    count += 1
else:
    print("Completed")
```

The `else` block will **not** execute.

---

# Nested While Loop

```python
i = 1

while i <= 3:
    j = 1

    while j <= 2:
        print(i, j)
        j += 1

    i += 1
```

Output

```
1 1
1 2
2 1
2 2
3 1
3 2
```

---

# User Input Example

```python
password = ""

while password != "python":
    password = input("Enter password: ")

print("Access Granted")
```

---

# Menu Driven Program

```python
choice = ""

while choice != "4":
    print("1. Add")
    print("2. Delete")
    print("3. View")
    print("4. Exit")

    choice = input("Choose: ")

print("Program Closed")
```

---

# Practical Examples

## Sum of Numbers

```python
total = 0
number = 1

while number <= 5:
    total += number
    number += 1

print(total)
```

Output

```
15
```

---

## Print Even Numbers

```python
number = 2

while number <= 20:
    print(number)
    number += 2
```

---

## Print Odd Numbers

```python
number = 1

while number < 20:
    print(number)
    number += 2
```

---

## Multiplication Table

```python
number = 8
i = 1

while i <= 10:
    print(number, "x", i, "=", number * i)
    i += 1
```

---

## Reverse Countdown

```python
count = 10

while count >= 1:
    print(count)
    count -= 1
```

---

## Reverse a String

```python
text = "Python"
index = len(text) - 1

while index >= 0:
    print(text[index])
    index -= 1
```

Output

```
n
o
h
t
y
P
```

---

## Find Factorial

```python
number = 5
factorial = 1

while number > 0:
    factorial *= number
    number -= 1

print(factorial)
```

Output

```
120
```

---

## Guess the Number

```python
secret = 7
guess = 0

while guess != secret:
    guess = int(input("Guess the number: "))

print("Correct!")
```

---

## Calculate Digits

```python
number = 98765
count = 0

while number > 0:
    count += 1
    number //= 10

print(count)
```

Output

```
5
```

---

## Reverse a Number

```python
number = 1234
reverse = 0

while number > 0:
    digit = number % 10
    reverse = reverse * 10 + digit
    number //= 10

print(reverse)
```

Output

```
4321
```

---

# Common Beginner Mistakes

## 1. Forgetting to Update the Variable

❌ Wrong

```python
i = 1

while i <= 5:
    print(i)
```

This creates an infinite loop.

✅ Correct

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

---

## 2. Forgetting the Colon

❌ Wrong

```python
while i < 5
    print(i)
```

✅ Correct

```python
while i < 5:
    print(i)
```

---

## 3. Wrong Indentation

❌ Wrong

```python
while i < 5:
print(i)
```

✅ Correct

```python
while i < 5:
    print(i)
```

---

## 4. Using Assignment Instead of Comparison

❌ Wrong

```python
while i = 5:
    print(i)
```

✅ Correct

```python
while i == 5:
    print(i)
```

---

# While vs For Loop

| Feature | while | for |
|----------|--------|------|
| Based on condition | ✅ | ❌ |
| Iterates over iterable | ❌ | ✅ |
| Number of iterations known | Not required | Usually known |
| Risk of infinite loop | High | Low |
| Best for user input | ✅ | ❌ |

---

# Time Complexity

| Operation | Complexity |
|-----------|------------|
| Loop n times | O(n) |
| Nested while loops | O(n²) |
| Constant work per iteration | O(n) |

---

# Interview Questions

### What is a `while` loop?

A `while` loop repeatedly executes code while a condition remains `True`.

---

### When should you use a `while` loop?

Use it when the number of iterations is **unknown** or depends on a condition.

---

### What causes an infinite loop?

When the loop condition never becomes `False`.

---

### What does `break` do?

It immediately exits the loop.

---

### What does `continue` do?

It skips the current iteration and moves to the next one.

---

### When does the `else` block execute?

Only when the loop finishes normally (without a `break`).

---

### Can a `while` loop be nested?

Yes.

```python
while condition1:
    while condition2:
        pass
```

---

# Quick Summary

- `while` loops execute as long as a condition is `True`.
- Always update the loop variable to avoid infinite loops.
- Use `break` to exit the loop.
- Use `continue` to skip the current iteration.
- Use `pass` as a placeholder.
- The `else` block runs only if the loop ends without `break`.
- `while` loops are ideal when the number of iterations is unknown.

---

## What's Next?

The next topic is **Loop Control Statements (`break`, `continue`, and `pass`)**, where you'll learn how to control the execution flow of loops.