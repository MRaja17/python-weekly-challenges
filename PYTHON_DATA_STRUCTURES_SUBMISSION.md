# Python Data Structures — Assignment Submission

## Easy 1 — Key concept (in my own words)
Python data structures are ways to organize and store data so we can access and modify it efficiently.
The most common built-in data structures are:
- **List**: ordered, mutable collection (good for sequences)
- **Tuple**: ordered, immutable collection (good for fixed records)
- **Set**: unordered collection of unique items (good for fast membership + deduplication)
- **Dict**: key → value mapping (good for fast lookup by key)

Choosing the right structure improves readability and performance (time + memory).

---

## Easy 2 — Toy example using Python Data Structures
Toy problem: Given a list of words, count frequency of each word.

Example:
Input: ["apple","banana","apple","orange","banana","apple"]
Output: {"apple":3, "banana":2, "orange":1}

```python
words = ["apple","banana","apple","orange","banana","apple"]
freq = {}
for w in words:
    freq[w] = freq.get(w, 0) + 1
print(freq)
