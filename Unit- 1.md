🧠 UNIT 1: Relational Model, Algebra & Database Design

📌 1. What are the Three Levels of Abstraction in Data Modeling?
🔹 **1. External Level** – What users see. (E.g., Only student names and marks)
🔹 **2. Conceptual Level** – Logical structure. (E.g., Student table with fields)
🔹 **3. Internal Level** – How data is stored. (E.g., Indexes, file system)

🧠 *Example:* Think of a library:
- External: User sees only book names
- Conceptual: System knows Author, Title, Genre
- Internal: Stored in a hard disk file

📎 Memory Trick: **E-C-I** (External, Conceptual, Internal)

---

📌 2. What is a Tuple, Key, Schema, and Attribute?
🔹 **Tuple**: A row in a table  
🔹 **Attribute**: A column (field) in a table  
🔹 **Key**: Unique ID (like Roll No)  
🔹 **Schema**: Structure of a table

🧠 *Example:* Student(RollNo, Name, City)  
- Tuple: (101, Ravi, Bhopal)  
- Attribute: RollNo  
- Key: RollNo  
- Schema: Student(RollNo, Name, City)

📎 Memory Trick: **T-A-K-S** = Tuple, Attribute, Key, Schema

---

📌 3. What is Normalization? (With Functional & Multivalued Dependency)
🔹 **Normalization** = Remove repetition, make DB efficient
🔹 **Functional Dependency** = One column decides another  
    ➤ E.g., RollNo → Name (RollNo determines Name)
🔹 **Multivalued Dependency** = One attribute determines many values  
    ➤ E.g., Student can have many phone numbers

🧠 *Example:*  
📦 Unnormalized: Ravi - Math, Science  
📦 Normalized:  
   Ravi - Math  
   Ravi - Science  

📎 Steps: 1NF → 2NF → 3NF → BCNF

---

📌 4. Relational Algebra Operations (with Symbols)
| Operation      | Symbol | Example                                   |
|----------------|--------|-------------------------------------------|
| Selection      | σ      | σ City='Bhopal'(Student)                  |
| Projection     | π      | π Name(Student)                           |
| Union          | ∪      | Student ∪ Teacher                         |
| Set Difference | −      | Student − Alumni                          |
| Cartesian Prod | ×      | Student × Course                          |
| Join           | ⨝      | Student ⨝ Course using RollNo             |

🧠 *Example:*  
- π Name(Student) → Just names of all students  
- σ City='Bhopal'(Student) → Students in Bhopal  

📎 Tip: Remember symbol + one-line use

---

📌 5. Write Relational Algebra Queries:
- Find students in “New Delhi”:  
  ➤ σ Address='New Delhi'(Student)
- Find teachers teaching DBMS:  
  ➤ σ Teaching_Subject='DBMS'(Teacher)
- Insert Teacher:  
  ➤ INSERT INTO Teacher VALUES(501, 'Amit', 'Math')
- Delete students from Mumbai:  
  ➤ DELETE FROM Student WHERE Address='Mumbai'

🧠 *Example:* Use city, subject, or name with SELECT/INSERT/DELETE

---

📌 6. What is BCNF? Why is it better than 3NF?
🔹 **BCNF** = Advanced version of 3NF  
🔹 Removes hidden dependency  
🔹 In 3NF, non-prime attributes depend on non-key

🧠 *Example:*  
Table: (StudentID, Course, Faculty)  
Issue: Faculty depends only on Course, not StudentID → Not BCNF

📎 BCNF Rule: **Every determinant must be a candidate key**

---


