🧠 UNIT 1: Relational Model, Relational Algebra & Database Design

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q1. What are the Three Levels of Abstraction in DBMS?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🧾 Definition:
Three levels define how data is viewed or stored in a database system.

🔸 External Level – What the user sees  
🔸 Conceptual Level – Logical structure of the whole database  
🔸 Internal Level – How data is physically stored in files/indexes

📦 Example:
Library System  
- External: Book Title  
- Conceptual: Book(Title, Author, Price)  
- Internal: Stored in disk blocks with index

💡 Trick: E-C-I (External → Conceptual → Internal)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q2. What is Tuple, Attribute, Key, and Schema?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔸 Tuple = A row (record) → (101, Ravi, Bhopal)  
🔸 Attribute = A column → Name, Address  
🔸 Key = Unique identifier → RollNo  
🔸 Schema = Table structure → Student(RollNo, Name, City)

💡 Trick: T-A-K-S = Tuple, Attribute, Key, Schema

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q3. What is Normalization? With FD & MVD
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔸 Normalization = Process to remove data redundancy  
🔸 FD (Functional Dependency): A → B (RollNo → Name)  
🔸 MVD (Multivalued Dependency): A →→ B (Student →→ Phone)

📦 Example:  
Unnormalized: Ravi – DBMS, Java  
Normalized:  
- Ravi – DBMS  
- Ravi – Java

💡 Steps: 1NF → 2NF → 3NF → BCNF

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q4. Relational Algebra Operations
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
| Operation     | Symbol | Example                               | Purpose              |
|---------------|--------|---------------------------------------|----------------------|
| Selection     | σ      | σ(City='Bhopal')(Student)             | Filter rows          |
| Projection    | π      | π(Name)(Student)                      | Select columns       |
| Union         | ∪      | Student ∪ Alumni                      | Combine rows         |
| Difference    | −      | Student − Alumni                      | Subtract rows        |
| Cartesian Prod| ×      | Student × Course                      | Cross join           |
| Join          | ⨝      | Student ⨝ Course using RollNo         | Merge matching rows  |

💡 Tip: σ = row filter, π = column picker

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q5. Relational Algebra Practical Queries
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ i) Find students from "New Delhi"  
→ σ(Address = 'New Delhi')(Student)

✅ ii) Teachers who teach "DBMS"  
→ σ(Subject = 'DBMS')(Teacher)

✅ iii) Insert new Teacher  
→ SQL: INSERT INTO Teacher VALUES(501, 'Amit', 'Math');

✅ iv) Delete students from Mumbai  
→ SQL: DELETE FROM Student WHERE Address = 'Mumbai';

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔹 Q6. What is BCNF? Why is it better than 3NF?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔸 BCNF = Boyce-Codd Normal Form  
🔸 Every determinant should be a candidate key  
🔸 Removes all anomalies better than 3NF

📦 Example:  
Table(StudentID, Course, Faculty)  
- Faculty depends on Course, not StudentID → Not in BCNF

💡 Advantage: Removes hidden dependencies

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📝 SUMMARY TO REMEMBER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📌 E-C-I = 3 Abstraction Levels  
📌 T-A-K-S = Tuple, Attribute, Key, Schema  
📌 FDs & MVDs = Functional/Multivalued Dependencies  
📌 σ, π, ∪, −, ×, ⨝ = Algebra Symbols  
📌 BCNF = Best Normal Form with stricter rules
