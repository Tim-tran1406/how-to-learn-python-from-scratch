# 5. Input & output

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

"Output" means showing things to the user; "input" means getting things *from* the user.

## Output with `print()`

You've used `print()` already. A few extra tricks:

```python
print("Hello", "world")        # multiple values -> Hello world
print("a", "b", "c", sep="-")  # change the separator -> a-b-c
print("no newline", end=" ")   # don't go to a new line
print("same line")
```

Output:

```text
Hello world
a-b-c
no newline same line
```

- `print` puts a **space** between multiple values by default (change with `sep`).
- It ends with a **new line** by default (change with `end`).

The cleanest way to mix text and variables is an **f-string**:

```python
name = "Tim"
score = 95
print(f"{name} scored {score} points.")
```

```text
Tim scored 95 points.
```

## Input with `input()`

`input()` pauses the program, shows a prompt, and waits for the user to type something and press
Enter:

```python
name = input("What is your name? ")
print(f"Nice to meet you, {name}!")
```

If the user types `Tim`, the output is:

```text
What is your name? Tim
Nice to meet you, Tim!
```

## ⚠️ The big gotcha: input is always text

`input()` **always returns a string**, even if the user types a number. So this breaks:

```python
age = input("Your age: ")   # user types 20
print(age + 1)              # ERROR: can't add a number to text
```

Convert it to a number first with `int()` (or `float()`):

```python
age = int(input("Your age: "))   # now age is the number 20
print(f"Next year you'll be {age + 1}.")
```

```text
Your age: 20
Next year you'll be 21.
```

!!! tip "Remember the pattern"
    Reading a number from the user is almost always `int(input(...))` or `float(input(...))`.

## Recap

- `print()` shows output; tweak it with `sep` and `end`.
- Use **f-strings** to mix text and values cleanly.
- `input(prompt)` reads what the user types — **always as a string**.
- Wrap it in `int()` / `float()` when you need a number.

*Source: [Python docs — input()](https://docs.python.org/3/library/functions.html#input) and
[print()](https://docs.python.org/3/library/functions.html#print).*

:material-arrow-right: Next: [Comments & code style](06-comments-and-style.md)
