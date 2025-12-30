# Pandas Fundamentals — Assignment Submission

## Easy 1 — Key concept (in my own words)
Pandas is a Python library for working with structured data (tables). The main objects are:
- **Series**: a single column of data
- **DataFrame**: a table (rows + columns)

Pandas makes it easy to load data (CSV/Excel), clean it (missing values, duplicates),
transform it (filtering, sorting), and summarize it (groupby + aggregations).

Key ideas:
- Read/write data (read_csv, to_csv)
- Selecting columns/rows (loc/iloc)
- Handling missing data (isna, fillna, dropna)
- GroupBy + aggregation (groupby, mean, count, sum)
- Merge/Join (merge) for combining tables

---

## Easy 2 — Toy example using Pandas
Toy problem: Create a small DataFrame of products and find the average price of items in stock.

```python
import pandas as pd

df = pd.DataFrame({
    "product": ["A", "B", "C"],
    "price": [10, 20, 30],
    "in_stock": [True, False, True]
})

avg_price_in_stock = df[df["in_stock"]]["price"].mean()
print("Average price (in stock):", avg_price_in_stock)
