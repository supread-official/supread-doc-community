# For Loop in Python

> Execute a block of code repeatedly by iterating over a sequence.

---

# What is a For Loop?

A `for` loop is used to iterate over a sequence such as:

- String
- List
- Tuple
- Set
- Dictionary
- Range
- Any iterable object

Instead of writing the same code multiple times, a `for` loop executes it automatically.

Example

```python
for i in range(5):
    print(i)
```

Output

```
0
1
2
3
4
```

---

# Syntax

```python
for variable in iterable:
    # Code to execute
```

Example

```python
fruits = ["Apple", "Banana", "Mango"]

for fruit in fruits:
    print(fruit)
```

Output

```
Apple
Banana
Mango
```

---

# How a For Loop Works

```python
numbers = [10, 20, 30]

for number in numbers:
    print(number)
```

Flow

```
Start
   ↓
Take first item
   ↓
Execute code
   ↓
Take next item
   ↓
Repeat until no items remain
```

---

# Using range()

`range()` generates a sequence of numbers.

## range(stop)

```python
for i in range(5):
    print(i)
```

Output

```
0
1
2
3
4
```

---

## range(start, stop)

```python
for i in range(2, 6):
    print(i)
```

Output

```
2
3
4
5
```

---

## range(start, stop, step)

```python
for i in range(0, 11, 2):
    print(i)
```

Output

```
0
2
4
6
8
10
```

---

# Negative Step

```python
for i in range(10, 0, -1):
    print(i)
```

Output

```
10
9
8
7
6
5
4
3
2
1
```

---

# Loop Through a String

```python
text = "Python"

for letter in text:
    print(letter)
```

Output

```
P
y
t
h
o
n
```

---

# Loop Through a List

```python
languages = ["Python", "Java", "C++"]

for language in languages:
    print(language)
```

---

# Loop Through a Tuple

```python
numbers = (1, 2, 3)

for number in numbers:
    print(number)
```

---

# Loop Through a Set

```python
colors = {"Red", "Green", "Blue"}

for color in colors:
    print(color)
```

> **Note:** Sets are unordered, so the output order may vary.

---

# Loop Through a Dictionary

## Keys

```python
student = {
    "name": "Alice",
    "age": 20,
    "city": "Delhi"
}

for key in student:
    print(key)
```

Output

```
name
age
city
```

---

## Values

```python
for value in student.values():
    print(value)
```

---

## Key and Value

```python
for key, value in student.items():
    print(key, value)
```

Output

```
name Alice
age 20
city Delhi
```

---

# Using enumerate()

Returns both index and value.

```python
fruits = ["Apple", "Banana", "Mango"]

for index, fruit in enumerate(fruits):
    print(index, fruit)
```

Output

```
0 Apple
1 Banana
2 Mango
```

---

# Custom Starting Index

```python
for index, fruit in enumerate(fruits, start=1):
    print(index, fruit)
```

Output

```
1 Apple
2 Banana
3 Mango
```

---

# Using zip()

Iterate through multiple sequences together.

```python
names = ["Alice", "Bob", "Charlie"]
marks = [85, 90, 78]

for name, mark in zip(names, marks):
    print(name, mark)
```

Output

```
Alice 85
Bob 90
Charlie 78
```

---

# Nested For Loop

A loop inside another loop.

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

Output

```
0 0
0 1
1 0
1 1
2 0
2 1
```

---

# break Statement

Stops the loop immediately.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

Output

```
0
1
2
3
4
```

---

# continue Statement

Skips the current iteration.

```python
for i in range(6):
    if i == 3:
        continue
    print(i)
```

Output

```
0
1
2
4
5
```

---

# pass Statement

Placeholder for future code.

```python
for i in range(5):
    pass
```

---

# else with for Loop

The `else` block executes only if the loop finishes normally (without `break`).

```python
for i in range(5):
    print(i)
else:
    print("Loop Finished")
```

Output

```
0
1
2
3
4
Loop Finished
```

Example with `break`

```python
for i in range(5):
    if i == 3:
        break
else:
    print("Completed")
```

Nothing is printed from `else`.

---

# Looping Backwards

```python
for i in range(5, 0, -1):
    print(i)
```

Output

```
5
4
3
2
1
```

---

# Practical Examples

## Print Squares

```python
for i in range(1, 6):
    print(i ** 2)
```

Output

```
1
4
9
16
25
```

---

## Sum of Numbers

```python
total = 0

for i in range(1, 6):
    total += i

print(total)
```

Output

```
15
```

---

## Multiplication Table

```python
number = 7

for i in range(1, 11):
    print(number, "x", i, "=", number * i)
```

Output

```
7 x 1 = 7
...
7 x 10 = 70
```

---

## Count Characters

```python
text = "Python"

count = 0

for char in text:
    count += 1

print(count)
```

Output

```
6
```

---

## Find Even Numbers

```python
for i in range(2, 21, 2):
    print(i)
```

---

## Find Odd Numbers

```python
for i in range(1, 20, 2):
    print(i)
```

---

## Find Largest Number

```python
numbers = [10, 25, 8, 41, 17]

largest = numbers[0]

for number in numbers:
    if number > largest:
        largest = number

print(largest)
```

Output

```
41
```

---

## Iterate Through a File

```python
with open("data.txt") as file:
    for line in file:
        print(line.strip())
```

---

# Common Beginner Mistakes

## 1. Forgetting the Colon

❌ Wrong

```python
for i in range(5)
    print(i)
```

✅ Correct

```python
for i in range(5):
    print(i)
```

---

## 2. Wrong Indentation

❌

```python
for i in range(5):
print(i)
```

✅

```python
for i in range(5):
    print(i)
```

---

## 3. Modifying a List While Iterating

❌

```python
numbers = [1, 2, 3]

for number in numbers:
    numbers.remove(number)
```

This may skip elements.

✅ Better

```python
numbers = [1, 2, 3]

for number in numbers.copy():
    numbers.remove(number)
```

---

## 4. Off-by-One Errors

❌

```python
for i in range(1, 10):
    print(i)
```

This prints `1` to `9`, not `10`.

✅

```python
for i in range(1, 11):
    print(i)
```

---

# Time Complexity

| Operation | Complexity |
|-----------|------------|
| Iterate through n items | O(n) |
| Nested loops | O(n²) |
| Loop with constant work | O(n) |

---

# Interview Questions

### What is the difference between `for` and `while`?

- `for` is used when iterating over an iterable or a known sequence.
- `while` is used when looping until a condition becomes `False`.

---

### What does `range()` return?

It returns a **range object**, which generates numbers lazily instead of storing them all in memory.

---

### Can we modify the loop variable?

Yes, but changing it does not affect the next iteration.

```python
for i in range(5):
    i = 100
    print(i)
```

Output

```
100
100
100
100
100
```

The loop still runs exactly five times.

---

### Can a `for` loop iterate over dictionaries?

Yes.

```python
for key in student:
    print(key)
```

or

```python
for key, value in student.items():
    print(key, value)
```

---

### What is the purpose of `enumerate()`?

It returns both the index and the value while iterating.

---

### What is the purpose of `zip()`?

It combines multiple iterables and iterates over them together.

---

# Quick Summary

- `for` loops iterate over iterable objects.
- `range()` generates sequences of numbers.
- Use `break` to stop a loop.
- Use `continue` to skip the current iteration.
- Use `pass` as a placeholder.
- `else` runs only if the loop completes without `break`.
- `enumerate()` provides index and value.
- `zip()` iterates over multiple iterables simultaneously.
- Nested loops are useful for multidimensional data and pattern generation.

---

## What's Next?

The next topic is **While Loop**, where you'll learn how to repeat code based on a condition instead of iterating over a sequence.