# 2. Numbers & math

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

Python has two main number types:

- **`int`** — whole numbers: `42`, `-7`, `1000000`
- **`float`** — numbers with a decimal point: `3.14`, `-0.5`, `2.0`

## Arithmetic operators

```python
print(7 + 3)    # addition
print(7 - 3)    # subtraction
print(7 * 3)    # multiplication
print(7 / 3)    # division
print(7 // 3)   # floor division (drops the remainder)
print(7 % 3)    # modulo (the remainder)
print(7 ** 3)   # exponent (7 to the power of 3)
```

Output:

```text
10
4
21
2.3333333333333335
2
1
343
```

A few that surprise beginners:

- `/` **always gives a `float`**, even `6 / 2` is `3.0`.
- `//` is **floor division** — it divides and throws away the decimal part: `7 // 3` is `2`.
- `%` is **modulo** — the *remainder*: `7 % 3` is `1`. (Great for "is this number even?": `n % 2 == 0`.)
- `**` is **power**, not `^`.

## Order of operations

Python follows normal math rules (PEMDAS): `**` first, then `*` `/` `//` `%`, then `+` `-`.
Use parentheses to be explicit:

```python
print(2 + 3 * 4)      # 14  (multiplication first)
print((2 + 3) * 4)    # 20  (parentheses first)
```

## Mixing ints and floats

If you mix them, the result becomes a `float`:

```python
print(5 + 2.0)   # 7.0
print(type(5 + 2.0))
```

```text
7.0
<class 'float'>
```

## Handy built-in functions

```python
print(abs(-8))        # 8   — absolute value
print(round(3.14159, 2))  # 3.14 — round to 2 decimals
print(max(4, 9, 1))   # 9
print(min(4, 9, 1))   # 1
```

You can also **convert** between types:

```python
print(int(3.9))     # 3   — int() chops off the decimal (doesn't round!)
print(float(5))     # 5.0
print(int("42") + 1)  # 43 — turn text "42" into a number
```

!!! warning "Floats aren't perfectly precise"
    Try this:
    ```python
    print(0.1 + 0.2)
    ```
    ```text
    0.30000000000000003
    ```
    That's not a Python bug — it's how *all* computers store decimals (in binary). For money or
    exact values, you'll later use the `decimal` module. For now, just know it can happen.

## Recap

- Two number types: `int` (whole) and `float` (decimal).
- Operators: `+ - * /` and the tricky ones — `//` (floor), `%` (remainder), `**` (power).
- `/` always returns a float; mixing int+float gives a float.
- Useful tools: `abs()`, `round()`, `min()`, `max()`, and `int()`/`float()` conversion.

*Source: [Python docs — Numbers](https://docs.python.org/3/tutorial/introduction.html#numbers).*

:material-arrow-right: Next: [Strings](03-strings.md)
