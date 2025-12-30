# NumPy Fundamentals — Assignment Submission

## Easy 1 — Key concept (in my own words)
NumPy is a Python library designed for fast numerical computation. It provides the ndarray
(N-dimensional array) which stores data efficiently and allows vectorized operations.
NumPy avoids Python loops and uses optimized C code internally, making operations much faster
and memory-efficient compared to standard Python lists.

Key ideas:
- ndarray for numerical data
- Vectorized operations (no explicit loops)
- Broadcasting for operations on different shapes
- Efficient linear algebra and statistics functions

---

## Easy 2 — Toy example using NumPy
Toy problem: Given an array of numbers, filter values greater than 5 and compute their squares.

```python
import numpy as np

arr = np.array([1, 4, 6, 8, 3, 10])
filtered = arr[arr > 5]
squared = filtered ** 2

print("Filtered:", filtered)
print("Squared:", squared)
