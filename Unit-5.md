# UNIT 4: Advanced Database Models – OODBMS, ORDBMS, and Mobile Databases

---

## Q1. What is OODBMS (Object-Oriented Database Management System)?

**Definition:**  
OODBMS is a type of database that stores data as objects, similar to how it's represented in object-oriented programming languages like Java, C++, or Python.

### 📌 Why Use OODBMS?
- Real-world objects like videos, 3D models, CAD files are hard to store in relational tables.
- OODBMS stores objects **without converting** them into tables.

### 🔍 Key Features:
- Supports **classes and objects**
- Allows **inheritance, encapsulation, polymorphism**
- Stores complex data like lists, arrays, and nested objects

### 🧠 Example:
```cpp
class Product {
  int id;
  string name;
  float price;
}
```
In OODBMS, the entire object is stored directly.

### ✅ Use Cases:
- Engineering design (CAD systems)
- Animation and graphics tools
- Real-time simulations

---

## Q2. What are the Building Blocks of OODBMS?

| Term         | Description                                                 |
|--------------|-------------------------------------------------------------|
| **Class**    | Blueprint for creating objects                              |
| **Object**   | Instance of a class with actual data                        |
| **Attribute**| Fields or properties inside an object (like name, price)    |
| **Method**   | Functions that act on data (like calculatePrice())          |
| **Inheritance** | Ability of a class to derive from another                |

---

## Q3. What is ORDBMS (Object-Relational DBMS)?

**Definition:**  
ORDBMS combines features of traditional **RDBMS** with limited object-oriented capabilities.

### 📌 Why Use ORDBMS?
- When you want to keep using SQL and tables but still store **complex/custom data types**.

### 🔍 Key Features:
- Supports traditional SQL
- Allows custom types (like array, structure)
- Supports inheritance and encapsulation

### 🧠 Example (PostgreSQL):
```sql
CREATE TYPE Address AS (
  street TEXT,
  city TEXT,
  pincode TEXT
);
```
You can now use this `Address` type inside a table.

### ✅ Use Cases:
- Banking (custom account types)
- Logistics (complex shipment data)
- Telecom and healthcare records

---

## Q4. Compare RDBMS, OODBMS, ORDBMS

| Feature        | RDBMS               | OODBMS                    | ORDBMS                      |
|----------------|---------------------|----------------------------|-----------------------------|
| Data Format    | Tables (rows/columns)| Objects (like OOP code)    | Tables + Object features     |
| OOP Support    | No                  | Full                       | Partial                      |
| Language       | SQL                 | Programming (C++, Java)    | SQL + object extensions      |
| Use Case       | Business apps       | Multimedia, CAD, AI        | Hybrid applications          |
| Examples       | MySQL, Oracle       | ObjectStore, db4o          | PostgreSQL, Informix         |

---

## Q5. What is a Mobile Database?

**Definition:**  
A **Mobile Database** is a lightweight database designed to work on **mobile devices** like smartphones or tablets, allowing data access even without internet.

### 📌 Characteristics:
- **Works offline** and syncs when online
- Small, fast, and power-efficient
- Data is stored **locally** on the device
- Syncs with cloud or central DB when online

### ✅ Example:
- A doctor enters patient records in a tablet app offline.  
- Later, it syncs with the hospital database over Wi-Fi.

**Technologies:** SQLite (Android/iOS), Firebase (Cloud + Mobile)

---

## Q6. What is a Disaster-Proof Database?

**Definition:**  
A disaster-proof database is built to survive **system failures**, **natural disasters**, or **cyber-attacks** without losing data.

### 📌 Features:
- **Backups** taken regularly
- **Replication** (same data at multiple locations)
- **Failover systems** (auto switch to backup)
- **High availability** (24/7 uptime)

### ✅ Example:
Banking systems use mirrored servers in different cities.  
If one fails (earthquake, fire), the backup server takes over.

---

## ✅ Final Summary Table

| Topic             | Key Points                                                    |
|-------------------|---------------------------------------------------------------|
| OODBMS            | Stores full objects, supports full OOP, used in multimedia    |
| ORDBMS            | SQL-based + partial object support, used in hybrid apps       |
| RDBMS vs OODBMS   | Tables vs Object Storage                                      |
| Mobile DB         | Works on mobile devices, supports offline access              |
| Disaster-Proof DB | Backup, replication, and high availability for failure safety |

