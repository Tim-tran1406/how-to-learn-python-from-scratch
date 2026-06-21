# 2. Install Python & run your first program

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

You have two ways to run Python. Pick whichever feels easier — you can switch later.

## Option A — Zero install (recommended to start)

Use the free **[Python Playground on Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ target=_blank }**.
It runs Python in your browser — nothing to install. Type code in a cell and press **▶** (or
`Shift`+`Enter`). This is the fastest way to start *today*.

## Option B — Install Python on your computer

When you're ready to run Python locally:

1. Go to **[python.org/downloads](https://www.python.org/downloads/)**.
2. Download the latest **Python 3** version for your system.
3. Run the installer.

!!! warning "Windows users: tick 'Add Python to PATH'"
    On the first screen of the Windows installer, check the box **"Add Python to PATH"** before
    clicking Install. It saves a lot of headaches later.

Check it worked by opening a terminal (Terminal on Mac, Command Prompt on Windows) and typing:

```bash
python3 --version
```

You should see something like `Python 3.12.x`.

## Your first program

Let's run the traditional first program every coder writes. In Colab (or a file called
`hello.py`), type:

```python
print("Hello, world!")
```

Run it. The output is:

```text
Hello, world!
```

🎉 **You just wrote and ran a program!** Let's understand it:

- `print(...)` is a **function** — a built-in command that displays whatever you put inside the
  parentheses.
- `"Hello, world!"` is a **string** — text, which always goes inside quotes.

## Try it yourself

Change the message and run it again:

```python
print("My name is Tim and I'm learning Python!")
```

!!! tip "Experiment"
    What happens if you forget the quotes, like `print(Hello)`? Try it — you'll get an **error**.
    Reading and understanding errors is a real skill you'll build throughout this course, so don't
    be afraid of them.

## Recap

- The easiest way to start is the **Colab Playground** (no install).
- To install locally, get **Python 3** from python.org (Windows: *Add Python to PATH*).
- `print("...")` displays text; text goes inside **quotes**.

:material-arrow-right: Next: [How to use this course](03-how-to-use-this-course.md)
