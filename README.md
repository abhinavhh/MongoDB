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
