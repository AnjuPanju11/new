# UNIT 3: Distributed Databases & Recovery

---

## Q1. What is DDBMS? How is it better than Centralized DBMS?

**DDBMS (Distributed Database Management System):**
- A database where data is stored across multiple physical locations but appears as a single system.

### ✅ Advantages over Centralized DBMS:
- **Faster Access** – Data is closer to users
- **Improved Reliability** – One site failure won’t crash the whole system
- **Scalability** – Easy to add new locations
- **Local Autonomy** – Each site can manage its own data

**Example:**  
Google stores your emails across multiple data centers but shows them in one Gmail app.

---

## Q2. What is Deadlock? Explain Two-Phase Commit Protocol.

### 🔹 Deadlock:
Occurs when two or more transactions are waiting for each other to release locks.

**Example:**
- T1 locks A and waits for B  
- T2 locks B and waits for A  
- → DEADLOCK!

---

### 🔹 Two-Phase Commit Protocol (2PC):
Used to ensure **atomic transactions** across multiple sites.

**Phases:**
1. **Prepare Phase** – Coordinator asks all sites to prepare  
2. **Commit Phase** – If all vote YES → commit; else → rollback

**Use Case:**  
Bank transfer between branches stored at different locations.

---

## Q3. What is Recovery in Distributed Databases?

**Definition:**  
Recovery means restoring the DB to a consistent state after failure.

### Recovery Handles:
- Site failure
- Communication failure
- Transaction failure

### Techniques:
- **Write-Ahead Logging (WAL)**
- **Checkpoints**
- **Undo/Redo operations**

---

## Q4. What is Concurrency Control in DDBMS?

**Goal:**  
Ensure that multiple users/transactions can safely access data **simultaneously**.

### Common Problems:
- **Lost Update**  
- **Dirty Read**  
- **Unrepeatable Read**

### Solutions:
- **Locking Protocols** (Two-phase locking)
- **Timestamps**
- **Commit Protocols (2PC)**

---

## Q5. Compare Centralized vs Hierarchical Deadlock Detection

| Feature                 | Centralized                 | Hierarchical                |
|-------------------------|-----------------------------|-----------------------------|
| Control Point           | Single global detector      | Multiple level detectors    |
| Fault Tolerance         | Low                         | High                        |
| Complexity              | Simple                      | Medium                      |
| Scalability             | Poor                        | Good                        |

**Summary:**
- Centralized = Simple, but risky if node fails  
- Hierarchical = Safer, more complex

---

## Q6. What is Data Replication & Fragmentation?

### 🔹 Replication:
- Copy of data stored at multiple sites
- Increases **availability** & **fault tolerance**

**Example:**  
Same customer table exists in Delhi and Mumbai branches.

### 🔹 Fragmentation:
- Splitting a table into parts (rows or columns)
- Improves **efficiency** by storing only what's needed

**Types:**
1. Horizontal Fragmentation (row-wise)
2. Vertical Fragmentation (column-wise)

---

## Summary to Remember:

| Topic                     | Key Idea                                |
|---------------------------|------------------------------------------|
| DDBMS                     | Data at multiple sites, acts like one DB |
| 2PC                       | Ensures all sites agree to commit        |
| Deadlock                 | Transactions waiting on each other       |
| Recovery                 | Restore DB after failure                 |
| Concurrency Control       | Allow safe parallel access               |
| Replication vs Fragment. | Copy vs Split of data                    |

