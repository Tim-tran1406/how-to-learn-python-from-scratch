# 6. Comments & code style

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

## Comments

A **comment** is a note in your code that Python ignores. It's for *humans* — to explain what's
going on. Start a comment with `#`:

```python
# Calculate the total price including 10% tax
price = 50
total = price * 1.10   # 1.10 adds 10%
print(total)
```

Python runs the code and skips everything after `#` on that line. Output:

```text
55.0
```

!!! tip "Comment the *why*, not the *what*"
    Good comments explain **why** something is done, not restate the obvious.
    ```python
    x = x + 1          # bad:  "add 1 to x"  (we can see that)
    retries = retries + 1   # good: meaningful name often needs no comment at all
    ```
    The best "comment" is often a clear variable name.

## Code style: PEP 8

Python has an official style guide called **PEP 8**. Following it makes your code look
professional and easy to read. The essentials:

- **Indentation:** use **4 spaces** per level (Python uses indentation to group code — it's not
  optional decoration!).
- **Naming:** `snake_case` for variables and functions (`total_price`, not `TotalPrice`).
- **Spaces around operators:** `x = 5 + 3`, not `x=5+3`.
- **One statement per line**, and keep lines reasonably short.

```python
# follows PEP 8 — clean and readable
first_name = "Tim"
age = 19
is_student = True

if is_student and age < 25:
    print(f"{first_name} gets the student discount.")
```

!!! note "Indentation actually matters in Python"
    In many languages, indentation is just for looks. In Python it's part of the **syntax** — it's
    how Python knows which lines belong inside an `if`, a loop, or a function. Wrong indentation is
    an error. (You'll see this in action in Part 3.)

## Recap

- Comments start with `#` and are ignored by Python — they're notes for humans.
- Comment the **why**, and prefer clear names over obvious comments.
- Follow **PEP 8**: 4-space indents, `snake_case`, spaces around operators.
- In Python, **indentation is part of the language**, not just style.

*Source: [PEP 8 — Style Guide for Python Code](https://peps.python.org/pep-0008/).*

:material-arrow-right: Next up (coming soon): **Part 3 · Control Flow**
