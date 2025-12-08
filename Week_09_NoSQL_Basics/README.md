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
Apply NoSQL Basics on a real dataset and explain results.

## Intermediate 2  
Implement NoSQL Basics using an appropriate library.

## Hard 1  
Optimize the NoSQL implementation for performance.

## Hard 2  
Build a mini project applying NoSQL Basics end-to-end.
