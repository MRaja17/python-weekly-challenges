# Week 09 – NoSQL Basics Challenges

## Easy 1  
NoSQL is a type of database that does not use the traditional tables and rows structure like SQL databases. 
Instead, NoSQL stores data in flexible formats such as documents, key–value pairs, wide-column stores, or graphs.

The key concept of NoSQL is:
- It handles unstructured or semi-structured data.
- It scales easily across many servers (horizontal scaling).
- It allows fast read/write operations for large datasets.
- It does not require a fixed schema, so data can change at any time.

In simple words, NoSQL gives more flexibility and speed for handling big and changing data compared to traditional SQL databases.


## Easy 2  
Let's take a simple toy example using a NoSQL document-based database like MongoDB.

### Example Scenario
We want to store information about a user.  
In SQL, we would need a fixed table with specific columns.  
In NoSQL (MongoDB), we can store the user as a flexible JSON-like document.

### NoSQL Document Example
{
  "name": "Meghana",
  "age": 25,
  "skills": ["Python", "SQL", "NoSQL"],
  "is_student": false
}

### Why this is NoSQL?
- There is no fixed schema → we can add/remove fields anytime.
- `skills` is an array → SQL cannot store this directly without extra tables.
- Fast read/write because it stores everything in a single document.

### Query Example (MongoDB)
To find all users with Python skill:


## Intermediate 1  
### Using a Real Dataset with NoSQL (MongoDB Example)

For this task, let's assume we have a small dataset of products stored in a NoSQL database (MongoDB).  
Each product is stored as a JSON-like document:

### Sample Dataset (products collection)
{
  "name": "iPhone 14",
  "brand": "Apple",
  "price": 799,
  "in_stock": true,
  "colors": ["black", "blue", "purple"]
}
{
  "name": "Galaxy S23",
  "brand": "Samsung",
  "price": 699,
  "in_stock": false,
  "colors": ["green", "cream"]
}
{
  "name": "Pixel 8",
  "brand": "Google",
  "price": 599,
  "in_stock": true,
  "colors": ["black"]
}

### **Queries Applied**

#### 1️⃣ Find all products in stock

## Intermediate 2  
### Implementing NoSQL Basics Using Python + PyMongo

For this implementation, we use **MongoDB** (a popular NoSQL database) and the Python library **PyMongo** to insert, query, and update NoSQL documents.

### 1️⃣ Install PyMongo
```bash
pip install pymongo
from pymongo import MongoClient

client = MongoClient("mongodb://localhost:27017/")
db = client["storeDB"]
products = db["products"]
sample_data = [
    {"name": "iPhone 14", "brand": "Apple", "price": 799, "in_stock": True, "colors": ["black", "blue", "purple"]},
    {"name": "Galaxy S23", "brand": "Samsung", "price": 699, "in_stock": False, "colors": ["green", "cream"]},
    {"name": "Pixel 8", "brand": "Google", "price": 599, "in_stock": True, "colors": ["black"]}
]

products.insert_many(sample_data)
in_stock_items = products.find({"in_stock": True})
for item in in_stock_items:
    print(item)
cheap_items = products.find({"price": {"$lt": 700}})
for item in cheap_items:
    print(item)
black_items = products.find({"colors": "black"})
for item in black_items:
    print(item)
products.update_one(
    {"name": "Galaxy S23"},
    {"$set": {"in_stock": True}}
)
products.delete_one({"name": "Pixel 8"})







## Hard 1  
### Optimizing NoSQL Implementation for Performance

To improve the performance of our NoSQL database (MongoDB), we apply key optimization techniques. These optimizations help speed up queries, reduce load, and make the database scalable for large datasets.

---

## 1️⃣ Create Indexes for Fast Querying

Indexes allow the database to look up results much faster.

### Example: Create an index on the "price" field
```python
products.create_index("price")
products.create_index("colors")
products.find(
    {"in_stock": True},
    {"name": 1, "price": 1, "_id": 0}
)
products.insert_many(sample_data, ordered=False)




## Hard 2  
Build a mini project applying NoSQL Basics end-to-end.
