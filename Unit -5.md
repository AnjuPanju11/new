# UNIT 5: Data Warehousing, OLAP, and Data Mining

---

## Q1. What is a Data Warehouse?

**Definition:**  
A Data Warehouse is a **centralized system** used to store **large volumes of historical data** for **analysis and reporting**.

### 📌 Key Features:
- Subject-Oriented (e.g., sales, customers)
- Integrated (collected from multiple sources)
- Time-variant (keeps historical data)
- Non-volatile (read-only, not updated frequently)

### ✅ Example:
Flipkart stores 5 years of customer orders in a data warehouse to analyze buying trends.

---

## Q2. What are the Components of a Data Warehouse?

| Component           | Description                                                |
|---------------------|------------------------------------------------------------|
| **Source Systems**   | Operational databases (e.g., Sales DB, HR DB)              |
| **ETL Tools**        | Extract, Transform, Load – cleans and loads data           |
| **Staging Area**     | Temporary area to clean/transform data                     |
| **Data Warehouse DB**| Central database that stores processed data                |
| **Metadata**         | Data about the data (who, when, what)                      |
| **OLAP Tools**       | Used to analyze data (pivot, slice, dice)                  |

---

## Q3. What is a Data Mart? How is it different from a Data Warehouse?

### 📘 Data Mart:
- A **smaller, focused version** of a data warehouse
- Contains data for **specific department or business area**

| Feature         | Data Warehouse            | Data Mart                       |
|-----------------|---------------------------|----------------------------------|
| Scope           | Organization-wide         | Department-level (e.g., Sales)   |
| Size            | Very Large                | Smaller                         |
| Example         | All company data          | Only sales data                 |

---

## Q4. What is OLAP (Online Analytical Processing)?

**Definition:**  
OLAP is a tool that helps users to **analyze data quickly** from multiple perspectives (dimensions).

### 📌 OLAP Operations:
- **Roll-up:** Summarize data (e.g., daily → monthly)
- **Drill-down:** View detailed data (e.g., monthly → daily)
- **Slice:** Filter one dimension (e.g., only for "2023")
- **Dice:** Filter multiple dimensions (e.g., 2023 + Product A)
- **Pivot:** Rotate dimensions (change rows to columns)

### ✅ Example:
Analyze total sales by region and time:
- Slice → Region = "North"
- Drill-down → See sales per day

---

## Q5. What is Data Mining?

**Definition:**  
Data Mining is the process of **finding hidden patterns or insights** in large datasets using mathematical and AI techniques.

### ✅ Real-Life Uses:
- Amazon recommends products (based on your past orders)
- Credit card companies detect fraud
- Healthcare predicts disease outbreaks

---

## Q6. Explain Association Rule Mining. Give 2 algorithms.

**Association Rule:**  
If a person buys **X**, they are likely to buy **Y**.

### 🛒 Example:
"If someone buys bread and butter → 80% chance they buy jam."

### 🔍 Algorithms:
1. **Apriori Algorithm** – Finds frequent item sets using multiple scans  
2. **FP-Growth (Frequent Pattern Growth)** – Faster, avoids scanning database again

---

## Q7. What is Predictive Data Mining?

**Definition:**  
It uses **existing data** to **predict future outcomes** using machine learning or statistics.

### ✅ Example:
- Predict which student might fail
- Forecast product sales next month
- Estimate customer churn rate

---

## Q8. What is a Knowledge-Based System?

**Definition:**  
A system that uses **stored knowledge** (rules, facts, logic) to solve problems intelligently.

### 🔍 Components:
- Knowledge Base (facts + rules)
- Inference Engine (logic/reasoning)
- User Interface (how users interact)

### ✅ Example:
- Medical diagnosis software (like AI chatbot for doctors)
- Chatbots, expert systems in finance

---

## Q9. What is a Spatial Database?

**Definition:**  
A Spatial DB stores and queries **geographic or location-based data** like maps, GPS coordinates, etc.

### ✅ Examples:
- Google Maps
- Uber ride tracking
- GIS applications

---

## Q10. What is E-R Design in context of Warehousing?

**Definition:**  
ER (Entity-Relationship) Design helps in modeling warehouse data like **dimensions**, **facts**, and **hierarchies**.

### 📦 Example in Warehouse:
- Entity: Product, Customer, Region  
- Relationship: Orders, Shipments

---

## ✅ Final Summary Table

| Concept              | Key Point                                      |
|----------------------|------------------------------------------------|
| Data Warehouse       | Central system for storing and analyzing data  |
| Data Mart            | Small, department-focused warehouse            |
| OLAP                 | Analyze data quickly via roll-up, slice, dice  |
| Data Mining          | Find patterns like “X → Y”                     |
| Predictive Mining    | Forecast future trends using past data         |
| Association Rule     | If buy A → likely to buy B                     |
| FP-Growth            | Fast algorithm to find frequent patterns       |
| Spatial DB           | Used for maps and location-based apps          |
| Knowledge Base       | Uses facts and rules to answer smartly         |

