🔵 Q1. OODBMS kya hota hai? (Object-Oriented Database)
🧠 Simple Definition:
OODBMS ek aisa database hai jisme data ko object ki tarah store karte hain — jaise programming me class-object banate hain (Java, C++, Python me).

💡 Samjho aise:
Jaise ek product ho — uska naam, price, ID sab ek sath store karna hai.
OODBMS me is poore object ko ek sath store karte hain, table me tod ke nahi.

cpp
Copy
Edit
class Product {
  int id;
  string name;
  float price;
}
Yeh pura object direct database me store ho sakta hai.

⭐ Kya-kya support karta hai?
Class & Object

Inheritance (jaise ek class dusri se cheeze le leti hai)

Polymorphism, Encapsulation

Complex data: list, array, object ke andar object

📌 Kaha use hota hai?
CAD design software (engineering)

Animation tools

Gaming aur Real-time simulations

🔵 Q2. OODBMS ke Main Parts (Building Blocks)
Term	Matlab kya hai? (Simple Language)
Class	Ek design/blueprint — jaise ek recipe ka format
Object	Class ka actual piece — jaise ek real product
Attribute	Data field — jaise name, price
Method	Function — jaise calculatePrice()
Inheritance	Ek class dusri class ki properties le sakti hai

🔵 Q3. ORDBMS kya hota hai? (Object-Relational DBMS)
🧠 Simple Definition:
ORDBMS me table bhi hoti hain aur object wali features bhi.
Matlab: Relational DB + thoda object wali power.

💡 Samjho aise:
Agar tu SQL use kar raha hai, lekin tujhe kuch complex cheeze store karni hain (jaise address, photo, custom types), to ORDBMS ka use karega.

sql
Copy
Edit
CREATE TYPE Address AS (
  street TEXT,
  city TEXT,
  pincode TEXT
);
Yeh custom type ko SQL table me use kar sakte ho.

✅ Kaha use hota hai?
Bank (Account details complex hoti hai)

Logistic (shipment ke details)

Healthcare (medical record structures)

🔵 Q4. RDBMS vs OODBMS vs ORDBMS – Easy Comparison
Feature	RDBMS	OODBMS	ORDBMS
Data Format	Table (row-column)	Object (OOP jaisa)	Table + Object features
OOP Support	❌ Nahi	✅ Full Support	⚠️ Thoda bahut
Language	SQL	Java, C++, Python	SQL + Custom Object Support
Kaha Use?	Business apps	CAD, Games, AI	Banking, Logistics, Hybrid
Example	MySQL, Oracle	ObjectStore, db4o	PostgreSQL, Informix

🔵 Q5. Mobile Database kya hota hai?
🧠 Simple Definition:
Mobile database aise database hote hain jo mobile me kaam karte hain — bina internet ke bhi.

📲 Khaas Baat:
Offline kaam karta hai

Data device me hi save hota hai

Internet aate hi cloud ya main DB se sync ho jata hai

Fast aur battery-efficient hota hai

✅ Example:
Doctor tablet me patient details likh raha hai bina net ke.
Later jab net aata hai, sab data hospital DB me chala jaata hai.

🛠️ Technologies: SQLite, Firebase

🔵 Q6. Disaster-Proof Database kya hota hai?
🧠 Simple Definition:
Yeh aise database hote hain jo kisi bhi system failure, natural disaster ya cyber attack ke baad bhi data ko safe rakhte hain.

📌 Kaise?
Backup system — data ka copy banta rahta hai

Replication — ek se jyada jagah same data

Failover — agar ek server down, to dusra ready

High availability — system 24/7 chalta rahe

✅ Example:
Bank ke 2 server — ek Mumbai, ek Delhi me.
Mumbai wala down ho gaya to Delhi ka backup turant kaam shuru karega.

🟢 Final Super-Simple Summary Table
Topic	Short & Sweet Notes
OODBMS	Object store karta hai, programming jaisa, multimedia me use
ORDBMS	SQL + thoda object support, bank/logistics ke liye best
RDBMS vs OODBMS	Table vs Object
Mobile DB	Phone/tablet me offline kaam, baad me sync hota hai
Disaster-Proof DB	Backup + failover + safe from any disaster

