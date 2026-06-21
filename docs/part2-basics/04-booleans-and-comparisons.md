# 4. Booleans & comparisons

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

A **boolean** (`bool`) has only two possible values: `True` or `False` (capitalized). Booleans are
how your programs make decisions.

## Comparisons produce booleans

When you compare two values, you get back `True` or `False`:

```python
print(5 > 3)     # True
print(5 == 5)    # True   (== means "is equal to")
print(5 != 3)    # True   (!= means "is not equal to")
print(2 >= 9)    # False
```

The comparison operators:

| Operator | Means |
|----------|-------|
| `==` | equal to |
| `!=` | not equal to |
| `>` `<` | greater / less than |
| `>=` `<=` | greater-or-equal / less-or-equal |

!!! warning "`=` vs `==` — the #1 beginner mistake"
    `=` **assigns** a value (`x = 5`). `==` **compares** (`x == 5` asks "is x equal to 5?"). Mixing
    them up is the most common early bug. Assign with one `=`, compare with two `==`.

## Combining conditions: `and`, `or`, `not`

```python
age = 20
print(age > 18 and age < 65)   # True  — BOTH must be true
print(age < 13 or age > 65)    # False — at least ONE must be true
print(not age > 18)            # False — flips True/False
```

- **`and`** → `True` only if *both* sides are true.
- **`or`** → `True` if *at least one* side is true.
- **`not`** → flips the value.

## Truthiness: values that "count as" True or False

Every value in Python is either "truthy" or "falsy" when used in a condition. The **falsy**
values are the empty/zero/nothing ones:

- `False`, `None`
- `0` and `0.0`
- `""` (empty string), `[]` (empty list), `{}` (empty dict)

Everything else is **truthy**. You can check with `bool()`:

```python
print(bool(0))       # False
print(bool(""))      # False
print(bool("hi"))    # True
print(bool(42))      # True
```

!!! tip "Why this is handy"
    Instead of `if len(name) > 0:` you can simply write `if name:` — an empty string is falsy, so
    it reads naturally as "if there is a name."

## Recap

- A `bool` is `True` or `False`.
- Comparisons (`==`, `!=`, `>`, `<`, `>=`, `<=`) return booleans.
- Combine with `and`, `or`, `not`.
- Empty/zero/`None` values are **falsy**; everything else is **truthy**.
- Assign with `=`, compare with `==`.

*Source: [Python docs — Boolean operations](https://docs.python.org/3/library/stdtypes.html#boolean-operations-and-or-not)
and [Truth value testing](https://docs.python.org/3/library/stdtypes.html#truth-value-testing).*

:material-arrow-right: Next: [Input & output](05-input-and-output.md)
