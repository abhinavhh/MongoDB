# 🍃 MongoDB Learning Journey

A structured repository for documenting my progress, notes, and exercises while learning MongoDB.

---

## 📚 Table of Contents
- [Concepts & Terminology](#-concepts--terminology)
- [Lessons Progress](#-lessons-progress)
  - [Lesson 01: The Basics](#lesson-01-the-basics)

---

## 💡 Concepts & Terminology

### SQL to MongoDB Mapping
If you're coming from a SQL background, here is how the core concepts translate:

| SQL Concept | MongoDB Equivalent | Description |
| :--- | :--- | :--- |
| Database | **Database** | A container for collections. |
| Table | **Collection** | A group of documents (typically related). |
| Row | **Document** | A single record (JSON-like format). |
| Column | **Field** | An attribute within a document. |
| Index | **Index** | Used to improve query performance. |

---

## 📖 Lessons Progress

### Lesson 01: The Basics
Understanding the core building blocks of a MongoDB database.

*   **Collections**: Instead of strictly typed tables, we use collections.
*   **Documents**: Records are stored as flexible documents (BSON) rather than fixed rows.
*   **Dynamic Schema**: Unlike SQL, documents in the same collection don't need to have the same fields.

Simple Example:

***Student Details***

```
{
    "name": "Rahul",
    "age": 23,
    "skills": ["React", "MongoDB"],
    "address": {
        "pincode": 670691,
        "location": Kerala
    }
}
```
### Lesson 02: Collections
Collections are actually like table, Database is the container holding collections

Simple Example:

***Gym System***
* **Collections**: Users, Trainers, Payment, Subscription, Plans, Diets etc.

### Lesson 03: BSON
Mongo DB already stores datas like json then why BSON.

***Because database needs more than readable text, it needs faster storage, faster parsing, more data types etc.***

```
{
  _id: ObjectId("6627abc123"),
  name: "Abhinav",
  joinedAt: ISODate("2026-04-22"),
  age: 24
}
```
* **_id**: Unique identifier for each document.
* **ObjectId**: 12-byte value that uniquely identifies a document.
* **ISODate**: Date and time value.

### Lesson 03.1 INSERT
Used to insert values into collections.

* **insertOne()**: To insert single row. Can used in sign ups.
* **insertMany()**: To insert many rows at once. Can use in multiple data imports for admins.

```
db.users.insertOne({
    name: "Arun",
    age: 20
})

db.users.insertMany([
    {name: "Arun",  age: 20},
    {name: "John",  age: 22},
])
```
#### Unique Indexing
When users sign up with same email needs to have a validation.

* **unique: true**: Make the field to have unique values.

```
db.users.createIndex(
  { email: 1 },
  { unique: true }
)
```

