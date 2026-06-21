# 3. Strings

[:material-rocket-launch: Run examples in Colab](https://colab.research.google.com/github/Tim-tran1406/how-to-learn-python-from-scratch/blob/main/notebooks/playground.ipynb){ .md-button target=_blank }

A **string** (`str`) is text. You create one by wrapping characters in quotes — single or double,
your choice (just be consistent):

```python
greeting = "Hello"
name = 'Tim'
```

Need a quote *inside* the text? Use the other kind on the outside:

```python
sentence = "It's a great day"   # single quote inside double quotes
```

For text spanning multiple lines, use **triple quotes**:

```python
poem = """Roses are red,
Python is fun."""
```

## Joining and repeating

```python
first = "Py"
second = "thon"
print(first + second)   # join with +  -> Python
print("ha" * 3)         # repeat with * -> hahaha
```

## f-strings: putting values into text (the modern way)

Put an `f` before the quotes, then drop variables inside `{ }`. This is the standard, readable way
to build text:

```python
name = "Tim"
age = 19
print(f"My name is {name} and I am {age} years old.")
```

Output:

```text
My name is Tim and I am 19 years old.
```

!!! tip "Prefer f-strings"
    f-strings (added in Python 3.6) are clearer and faster than older approaches like `+`
    gluing or `.format()`. Use them.

## Reaching into a string (indexing & slicing)

Each character has a position (an **index**) starting at **0**. Negative indexes count from the
end.

```python
word = "Python"
#       012345
print(word[0])    # P  — first character
print(word[-1])   # n  — last character
print(word[0:3])  # Pyt — characters 0,1,2 (the end index is NOT included)
print(word[2:])   # thon — from index 2 to the end
```

!!! note "Slicing stops *before* the end number"
    `word[0:3]` gives characters `0`, `1`, `2` — **not** `3`. This "up to but not including" rule
    is everywhere in Python, so it's worth remembering early.

## Useful string tools

```python
text = "  Hello, World  "

print(len(text))          # 16 — length (including spaces)
print(text.strip())       # "Hello, World" — remove surrounding spaces
print(text.upper())       # "  HELLO, WORLD  "
print(text.lower())       # "  hello, world  "
print("hello".replace("l", "L"))   # heLLo
print("a,b,c".split(","))          # ['a', 'b', 'c']  -> a list
print("Python".startswith("Py"))   # True
```

!!! warning "Strings can't be changed in place"
    Strings are **immutable** — methods like `.upper()` return a *new* string and leave the
    original untouched:
    ```python
    name = "tim"
    name.upper()       # makes "TIM" but throws it away
    print(name)        # still "tim"
    name = name.upper()  # reassign to actually keep it
    print(name)        # TIM
    ```

## Special characters

Inside strings, a backslash starts an "escape": `\n` is a new line, `\t` is a tab.

```python
print("Line 1\nLine 2")
```

```text
Line 1
Line 2
```

## Recap

- Strings are text in quotes; triple quotes span multiple lines.
- Join with `+`, repeat with `*`.
- Use **f-strings** (`f"Hi {name}"`) to insert values.
- Index from `0` (and from `-1` at the end); slicing is **up to but not including** the end index.
- Handy methods: `len()`, `.strip()`, `.upper()`/`.lower()`, `.replace()`, `.split()`.
- Strings are **immutable** — methods return a new string.

*Source: [Python docs — Strings](https://docs.python.org/3/tutorial/introduction.html#text) and
[Text Sequence Type](https://docs.python.org/3/library/stdtypes.html#text-sequence-type-str).*

:material-arrow-right: Next up (coming soon): **Booleans & comparisons**
