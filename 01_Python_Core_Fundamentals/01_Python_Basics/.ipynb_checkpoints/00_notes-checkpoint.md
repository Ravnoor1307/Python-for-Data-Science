# Python Basics

> Module: 01 Python Basics  |  Topic notes  |  Read time: 12-15 minutes

## 1. What this topic is about

Python is an interpreted, dynamically typed language. Before you can analyse data you need fluency in its atoms: variables, literals, types, input and output.

Python Basics is one of the building blocks you will keep reaching for long after this module is finished. The goal of these notes is not to memorise syntax but to build a mental model: what problem does python basics solve, what does it cost, and when is a different tool the better answer. Work through the three notebooks in this folder in order - `01_concepts.ipynb` for the guided tour, `02_examples.ipynb` for worked real-world usage, and `03_exercises.ipynb` for deliberate practice with solutions and assertions.

## 2. Why it matters in a data science workflow

In production data work you are judged on correctness first and speed second. Python Basics shows up in the day-to-day loop of loading data, reshaping it, modelling it and shipping it. Engineers who understand this topic deeply write shorter code, debug faster, and are able to explain their choices in a design review. Interviewers probe it because it separates candidates who have copied tutorials from candidates who have actually built something.

## 3. Core concepts

### 3.1 Variables and dynamic typing

A variable is a name bound to an object, not a labelled box. Rebinding a name never changes the old object; it points the name somewhere else. Types live on objects, which is why `x = 5` then `x = 'five'` is legal.

Practical angle: when you use variables and dynamic typing in a real project, be explicit about your assumptions and verify them with a quick check in code rather than trusting intuition. Small verification cells - printing shapes, dtypes, value counts or an `assert` - cost seconds and save hours. The notebooks in this folder demonstrate exactly that habit.

### 3.2 Numeric types

`int` has arbitrary precision, `float` is IEEE-754 double precision and therefore approximate, `complex` exists for signal work. Money should never be a float; use `decimal.Decimal`.

Practical angle: when you use numeric types in a real project, be explicit about your assumptions and verify them with a quick check in code rather than trusting intuition. Small verification cells - printing shapes, dtypes, value counts or an `assert` - cost seconds and save hours. The notebooks in this folder demonstrate exactly that habit.

### 3.3 Type conversion

Explicit conversion with `int()`, `float()`, `str()` and `bool()` is safe and readable. Implicit coercion in Python is deliberately minimal, which prevents a whole class of silent bugs.

Practical angle: when you use type conversion in a real project, be explicit about your assumptions and verify them with a quick check in code rather than trusting intuition. Small verification cells - printing shapes, dtypes, value counts or an `assert` - cost seconds and save hours. The notebooks in this folder demonstrate exactly that habit.

### 3.4 Input and output

`input()` always returns a string, so numeric input needs conversion. f-strings are the modern formatting tool and support alignment, precision and expressions.

Practical angle: when you use input and output in a real project, be explicit about your assumptions and verify them with a quick check in code rather than trusting intuition. Small verification cells - printing shapes, dtypes, value counts or an `assert` - cost seconds and save hours. The notebooks in this folder demonstrate exactly that habit.

## 4. Code you should be able to write from memory

**Names are bindings, not boxes**

```python
# Names are bindings, not boxes
a = 5
b = a          # both names point at the same int object
a = 'five'     # rebinding a leaves b untouched
print(a, b, type(a).__name__, type(b).__name__)
```

**int is arbitrary precision, float is not**

```python
# int is arbitrary precision, float is not
big = 2 ** 200
print('2**200 has', len(str(big)), 'digits')
print('0.1 + 0.2 ==', 0.1 + 0.2)
print('exactly equal to 0.3?', 0.1 + 0.2 == 0.3)
print('safe comparison:', math.isclose(0.1 + 0.2, 0.3))
```

**Money must not be a float**

```python
# Money must not be a float
from decimal import Decimal, getcontext
getcontext().prec = 10
price = Decimal('19.99')
qty = 3
print('float  :', 19.99 * 3)
print('decimal:', price * qty)
```

**Explicit conversion and its failure mode**

```python
# Explicit conversion and its failure mode
raw = '42'
print(int(raw) + 8)
for bad in ['4.5', 'abc', '']:
    try:
        int(bad)
    except ValueError as err:
        print(f'int({bad!r}) failed: {err}')
```

## 5. Common mistakes

1. Reaching for python basics before checking whether the data is in the shape the API expects. Inspect first, transform second.
2. Copying a snippet without reading its assumptions, then debugging the symptom instead of the cause.
3. Skipping the verification step, so an error propagates several cells downstream where it is much harder to locate.
4. Optimising for cleverness instead of readability. The reviewer of your code is usually you, three months later.
5. Not writing down what you learned. Keep a short log per topic in `24_Notes_and_Resources/`.

## 6. Interview angle

- Explain variables and dynamic typing to someone who has never seen it, in under a minute, then give one example where it fails.
- Explain numeric types to someone who has never seen it, in under a minute, then give one example where it fails.
- Explain type conversion to someone who has never seen it, in under a minute, then give one example where it fails.
- Explain input and output to someone who has never seen it, in under a minute, then give one example where it fails.

## 7. Self check

You are done with this topic when you can:

- [ ] Use variables and dynamic typing correctly without looking at the docs
- [ ] Use numeric types correctly without looking at the docs
- [ ] Use type conversion correctly without looking at the docs
- [ ] Use input and output correctly without looking at the docs
- [ ] Finish every exercise in `03_exercises.ipynb` with all assertions passing
- [ ] Explain the topic aloud with a whiteboard example

## 9. Datasets used

- [No external dataset - pure Python](https://docs.python.org/3/tutorial/)

## Files in this folder

| File | Purpose |
| --- | --- |
| `00_notes.md` | These notes |
| `01_concepts.ipynb` | Guided tour of every concept above |
| `02_examples.ipynb` | Worked real-world examples |
| `03_exercises.ipynb` | Practice problems with solutions |
