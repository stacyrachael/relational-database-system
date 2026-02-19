# Database Normalization

## Objective
To design a database that reduces redundancy and ensures data integrity.

---

## First Normal Form (1NF)
Rules:
- Each field contains atomic values
- No repeating groups
- Each record has a primary key

Applied:
- Student names separated into first_name and last_name
- Each table has a defined PRIMARY KEY

---

## Second Normal Form (2NF)
Rules:
- Must be in 1NF
- No partial dependency on composite keys

Applied:
- Course details stored separately from Students
- Enrollment table used to resolve many-to-many relationship

---

## Third Normal Form (3NF)
Rules:
- Must be in 2NF
- No transitive dependencies

Applied:
- Instructor stored in Courses table, not Students
- Grades linked via Enrollment instead of directly to Student

---

## Why This Matters
Normalization:
✔ Prevents duplicate data  
✔ Makes updates safer  
✔ Improves query performance  
✔ Reflects real-world relational structure

---

## Entity Relationships

Students ← Enrollments → Courses  
Enrollments → Grades

This structure allows scalable academic record management.
