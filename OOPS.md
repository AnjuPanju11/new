# 🎯 MCIT-103 – Object Oriented Technology (Smart Notes)

---

## 📌 Q1. Object-Oriented Basics
### a) What is Object-Oriented approach? Explain its four key characteristics.

🧠 **Definition:**
Object-Oriented Approach is a software design technique where everything is represented as an **object** that has **attributes (data)** and **methods (functions)**.

### 🔑 Characteristics:
1. **Encapsulation** – Data & methods are bundled together.  
2. **Abstraction** – Shows only essential details, hides internal complexity.  
3. **Inheritance** – One class can reuse properties of another.  
4. **Polymorphism** – Same function name behaves differently for different objects.

### 💻 Example in C++:
```cpp
class Animal {
public:
    void sound() { cout << "Animal makes sound"; }
};
class Dog : public Animal {
public:
    void sound() { cout << "Dog barks"; }
};
int main() {
    Animal *a = new Dog();
    a->sound(); // Output: Dog barks (Polymorphism)
}
```

---

### b) Explain ADT as Object Class
🧠 **Abstract Data Type (ADT)** is a data type where only operations are defined, implementation is hidden.

💻 **Example – Stack ADT:**
```cpp
class Stack {
    int arr[5], top;
public:
    Stack() { top = -1; }
    void push(int x) { arr[++top] = x; }
    int pop() { return arr[top--]; }
};
```

---

## 📌 Q2. UML & Modeling
### a) What is UML? Why is it needed?
🧠 **Definition:** UML (Unified Modeling Language) is a visual language for **modeling software systems**.

✅ **Basic Building Blocks:**
- **Things** – Class, Object, Interface, Collaboration  
- **Relationships** – Association, Generalization, Dependency  
- **Diagrams** – Class, Sequence, Use-case, Activity, etc.

---

### b) Structural Modeling in UML
📌 **Structural Modeling** shows the static structure of a system.  
📊 **Diagrams Used:**
- Class Diagram
- Object Diagram
- Component Diagram
- Deployment Diagram

---

## 📌 Q3. OODBMS vs RDBMS vs ORDBMS
🧠 **OODBMS:** Stores data as objects (like in C++/Java).  
🧠 **RDBMS:** Stores data in tables (rows & columns).  
🧠 **ORDBMS:** Combination of both (SQL + Object features).

| Feature       | RDBMS         | OODBMS       | ORDBMS            |
|--------------|--------------|--------------|-------------------|
| Data Format  | Table        | Object       | Table + Object    |
| OOP Support  | ❌ No        | ✅ Full      | ⚠️ Partial       |
| Example      | MySQL, Oracle | db4o, ObjectDB | PostgreSQL       |

💻 **Custom Type Example (ORDBMS – PostgreSQL):**
```sql
CREATE TYPE Address AS (
   street TEXT,
   city TEXT,
   pincode TEXT
);
CREATE TABLE Customers (
   id INT,
   name TEXT,
   addr Address
);
```

---

## 📌 Q4. Reusability & Software Development Stages
### a) Why Reusability is Important?
✔ Saves time, cost, & reduces errors.  
✔ Promotes modularity (code reuse via inheritance & polymorphism).

### b) Software Development Stages
1️⃣ Requirement Analysis  
2️⃣ Design  
3️⃣ Coding  
4️⃣ Testing  
5️⃣ Deployment  
6️⃣ Maintenance  

---

## 📌 Q5. UML Class Diagram (Bank ATM System)
💻 **Example Diagram (Text Format)**

```
+----------------+         +-----------------+
|   ATM Machine  |<>-------| Bank Database   |
+----------------+         +-----------------+
| location       |         | accountDetails  |
| insertCard()   |         | checkBalance()  |
| withdrawCash() |         | updateAccount() |
+----------------+         +-----------------+
```

---

## 📌 Q6. Relationships in UML
| Relationship   | Symbol | Meaning |
|---------------|--------|---------|
| Association   | Solid line | Basic link |
| Aggregation   | Empty diamond | Whole-part relationship |
| Composition   | Filled diamond | Strong whole-part |
| Generalization| Triangle arrow | Inheritance |

---

## 📌 Q7. Frameworks & Design Optimization
✔ **Framework** = Predefined structure for solving recurring problems.  
✔ **Design Optimization Tasks:** Reduce coupling, increase cohesion, reusable components.

---

## 📌 Q8. Advanced Topics
- **Distributed Object Computing** → Remote objects accessed via RMI/CORBA.  
- **Behavioral Modeling** → Shows interaction between objects.  
- **Coupling & Cohesion** → Good design = Low coupling + High cohesion.

---

# ✅ Final Exam Revision Tips:
✔ Learn **Key UML diagrams (Class + Sequence)**  
✔ Focus on **OODBMS vs RDBMS vs ORDBMS**  
✔ Revise **OOP Concepts (4 Pillars)**  
✔ Prepare **short notes on frameworks, patterns, relationships**  

