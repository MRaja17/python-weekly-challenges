# Python Basics & Setup — Assignment Submission

## Easy 1 — Key concept (in my own words)
Python Basics & Setup means installing Python and setting up a clean environment so code runs reliably.
It includes using a code editor (VS Code), managing packages with pip, and optionally using a virtual environment
so project dependencies don’t conflict. Python basics also include variables, data types, conditionals, loops,
functions, and reading/writing files.

Setup essentials:
- Python installed and working (`python --version`)
- VS Code + Python extension
- pip for installing libraries
- (Recommended) virtual environment: `python -m venv .venv`

---

## Easy 2 — Toy example (basic Python)
Toy problem: Given a list of numbers, filter even numbers and compute their squares.

Example:
Input: [1,2,3,4,5]
Even numbers: [2,4]
Squares: [4,16]

```python
nums = [1, 2, 3, 4, 5]
evens = [n for n in nums if n % 2 == 0]
squares = [n*n for n in evens]
print("evens:", evens)
print("squares:", squares)
