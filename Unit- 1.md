# UNIT 1: Relational Model, Relational Algebra & Database Design

---

## Q1. What are the Three Levels of Abstraction in DBMS?

**Definition:**  
Three levels define how data is viewed or stored in a database system.

### 1. External Level
- What the user sees (e.g., only names and marks)

### 2. Conceptual Level
- Logical structure of the full database (e.g., Student table with columns)

### 3. Internal Level
- How data is physically stored (e.g., files, indexes)

**Example: Library System**

- External: Book title
- Conceptual: Book(Title, Author, Price)
- Internal: Stored in disk blocks with indexing

**Memory Tip:** E → C → I  
(External → Conceptual → Internal)

---

## Q2. What is Tuple, Attribute, Key, and Schema?

| Term      | Meaning                          | Example                         |
|-----------|----------------------------------|---------------------------------|
| Tuple     | A row in a table                 | (101, Ravi, Bhopal)             |
| Attribute | A column in a table              | RollNo, Name                    |
| Key       | Uniquely identifies each record  | RollNo                          |
| Schema    | Table structure definition       | Student(RollNo, Name, Address)  |

**Memory Tip:** T-A-K-S = Tuple, Attribute, Key, Schema

---

## Q3. What is Normalization? With FD & MVD

**Normalization:** Process of reducing data redundancy.

- **Functional Dependency (FD):** A → B (e.g., RollNo → Name)
- **Multivalued Dependency (MVD):** A →→ B (e.g., Student →→ Phone)

**Example:**
Before Normalization:
```
Ravi – DBMS, Java
```
After Normalization:
```
Ravi – DBMS  
Ravi – Java
```

**Steps in Normalization:**  
1NF → 2NF → 3NF → BCNF

---

## Q4. Relational Algebra Operations

| Operation     | Symbol | Example                              | Purpose               |
|---------------|--------|--------------------------------------|-----------------------|
| Selection     | σ      | σ(City = 'Bhopal')(Student)          | Filter rows           |
| Projection    | π      | π(Name)(Student)                     | Select columns        |
| Union         | ∪      | Student ∪ Alumni                     | Combine rows          |
| Set Difference| −      | Student − Alumni                     | Subtract common rows  |
| Cartesian Prod| ×      | Student × Course                     | Cross join            |
| Join          | ⨝      | Student ⨝ Course using RollNo        | Combine matching rows |

**Quick Tip:**  
- Use `σ` for filtering rows  
- Use `π` for selecting columns

---

## Q5. Relational Algebra Queries

**Given Tables:**
- Student(RollNo, Name, Address)
- Teacher(TeacherID, TeacherName, Subject)

**Queries:**

1. Students from "New Delhi":
```
σ(Address = 'New Delhi')(Student)
```

2. Teachers who teach "DBMS":
```
σ(Subject = 'DBMS')(Teacher)
```

3. Insert a new Teacher (in SQL):
```sql
INSERT INTO Teacher VALUES(501, 'Amit', 'Math');
```

4. Delete students from Mumbai (in SQL):
```sql
DELETE FROM Student WHERE Address = 'Mumbai';
```

---

## Q6. What is BCNF? Why is it better than 3NF?

**BCNF (Boyce-Codd Normal Form):**
- A stronger version of 3NF
- Every determinant must be a candidate key

**Example:**
```
Table: (StudentID, Course, Faculty)
Faculty depends on Course → Not in BCNF
```

**Why BCNF is better:**
- Eliminates all types of redundancy
- More consistent and cleaner schema
