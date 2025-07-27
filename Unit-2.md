# UNIT 2: SQL, Query Processing & Optimization

---

## Q1. What is an SQL Query Block? Why is it important?

**Definition:**  
An SQL query block is the basic unit of an SQL query – it includes `SELECT`, `FROM`, `WHERE`, `GROUP BY`, etc.

**Structure of SQL Query Block:**
```sql
SELECT Name
FROM Student
WHERE City = 'Bhopal';
```

**Why important?**
- Helps in query planning and optimization
- Makes SQL modular and readable

---

## Q2. What is Query Optimization?

**Definition:**  
It is the process of improving the performance of a query by reducing its execution time and resource usage.

**Steps in Query Optimization:**
1. Parsing SQL into internal tree format
2. Translating into Relational Algebra
3. Generating different query plans
4. Estimating the cost of each plan
5. Selecting the lowest-cost plan

**Goal:**  
Execute query in **least time using minimum resources**

---

## Q3. What is a Query Evaluation Plan?

**Definition:**  
A query evaluation plan describes:
- The sequence of operations (scan, join, sort)
- The algorithms used (e.g., nested loop, merge join)
- The indexes or access paths used

**Example:**
For this query:
```sql
SELECT Name FROM Student WHERE City = 'Bhopal';
```
Plan might be:
- Index scan on City column
- Apply selection
- Output names

---

## Q4. What is Cost Estimation in Query Optimization?

**Definition:**  
Cost estimation involves predicting:
- I/O cost (disk access)
- CPU cost (comparison, sorting)
- Memory usage

**Parameters Considered:**
- Size of data
- Available indexes
- Number of rows scanned
- Join method used

**Example:**
Using an index might cost 10 disk accesses vs. 100 for full scan → index scan preferred

---

## Q5. What is Pipelining in Query Execution?

**Definition:**  
Pipelining means passing the output of one operation **directly** to the next without storing in intermediate tables.

**Benefits of Pipelining:**
- Saves disk I/O
- Faster execution
- Saves memory

**Example:**
Instead of:
- Select → store in temp table → project

Use:
- Select → directly project → final result

**Analogy:**  
Like streaming a video instead of downloading it fully before watching.

---

## SQL Quick Examples:

1. **SELECT with WHERE:**
```sql
SELECT Name FROM Student WHERE City = 'Indore';
```

2. **GROUP BY:**
```sql
SELECT City, COUNT(*) FROM Student GROUP BY City;
```

3. **JOIN Example:**
```sql
SELECT Student.Name, Teacher.TeacherName
FROM Student
JOIN College ON Student.RollNo = College.RollNo
JOIN Teacher ON College.TeacherID = Teacher.TeacherID;
```

---

## Summary to Remember:

| Concept              | Keyword          | Purpose                                      |
|----------------------|------------------|----------------------------------------------|
| SQL Block            | SELECT-FROM-WHERE| Basic structure of SQL query                 |
| Query Optimization   | Cost-based       | Find fastest and cheapest execution plan     |
| Evaluation Plan      | Tree of steps    | Shows how the DB will run the query          |
| Cost Estimation      | Disk, CPU, RAM   | Predicts performance of different plans      |
| Pipelining           | No temp storage  | Faster result processing by direct passing   |

