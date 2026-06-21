# 1. Variables & data types

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

## What is a variable?

A **variable** is a *name* that stores a *value* so you can use it later. Think of it as a
labelled box: you put something in the box and write a name on it.

You create a variable with `=` (the **assignment** operator):

```python
name = "Tim"
age = 19
```

Now `name` holds `"Tim"` and `age` holds `19`. Use them anywhere:

```python
print(name)
print(age)
```

Output:

```text
Tim
19
```

!!! note "`=` means 'store', not 'equals'"
    `age = 19` reads as *"put 19 into age."* It's an instruction, not a math statement. (To check
    if two things are equal, you'll later use `==`.)

## Python figures out the type for you

Unlike some languages, you don't declare what kind of value a variable holds — Python knows from
what you put in it. This is called **dynamic typing**. You can even change it:

```python
x = 10        # x is a number
x = "hello"   # now x is text — totally fine
```

## The core data types

These five cover almost everything you'll do at first:

| Type | Name | Example |
|------|------|---------|
| `int` | whole number | `42`, `-7`, `0` |
| `float` | decimal number | `3.14`, `-0.5` |
| `str` | text ("string") | `"hello"`, `'Python'` |
| `bool` | true/false | `True`, `False` |
| `NoneType` | "nothing" | `None` |

You can check any value's type with the built-in `type()` function:

```python
print(type(42))
print(type(3.14))
print(type("hello"))
print(type(True))
```

Output:

```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

## Naming variables

Rules (required):

- Use letters, numbers, and underscores (`_`) — but **can't start with a number**.
- Names are **case-sensitive**: `age` and `Age` are different.
- Can't use Python's reserved words (like `if`, `for`, `class`).

Convention (strongly recommended):

- Use lowercase words joined by underscores — called **snake_case**: `first_name`, `total_price`.

```python
first_name = "Tim"     # good ✅
totalPrice = 9.99      # works, but not the Python style
2cool = "nope"         # ERROR ❌ — can't start with a number
```

!!! tip "Name things clearly"
    `n = 19` works, but `age = 19` tells the reader what it *means*. Good names make your code
    explain itself.

## Recap

- A variable is a **name that stores a value**, created with `=`.
- Python is **dynamically typed** — it infers the type, and you can reassign freely.
- Core types: `int`, `float`, `str`, `bool`, `None`. Check with `type()`.
- Use **snake_case** and meaningful names.

*Source: [Python docs — An Informal Introduction](https://docs.python.org/3/tutorial/introduction.html).*

:material-arrow-right: Next: [Numbers & math](02-numbers-and-math.md)
