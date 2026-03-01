# 📚 DBMS Notes

---

## 🔹 Data vs Information

**Data = raw facts (unprocessed). It has no meaning by itself.**  
Data is a collection of raw, unorganized facts that by itself has no meaning.

**Information = processed data that has meaning.**  
Information is processed and organized data that is meaningful and useful for decision-making.

👉 **Data = input**  
👉 **Information = output**

**Summary:**  
Data is raw and unprocessed facts, whereas information is processed data that is meaningful and useful.

---

## 🔹 Database

**Database = organized collection of data**

A database is an organized collection of related data stored electronically for easy access and management.

**Stored so we can:**

- access easily  
- update easily  
- manage easily  

**Example: Your college system storing:**

- student details  
- marks  
- attendance  

👉 That storage = **Database**

---

## 🔹 DBMS

**DBMS = software that manages databases**

DBMS is software that enables users to efficiently store, retrieve, update, and manage data in a database.

**It helps to:**

- store data  
- retrieve data  
- update data  
- delete data  

**Examples of DBMS:**  
MySQL, Oracle, PostgreSQL, MongoDB

---

# ❌ Disadvantages of File System

---

## 1️⃣ Data Redundancy

👉 Same data stored multiple times

Student data stored in:

- admission.txt  
- library.txt  
- hostel.txt  

Same student info repeated.

**Result → duplicate data**

---

## 2️⃣ Data Inconsistency

👉 Same data has different values in different files

**Example:**

- File A: Rahul age = 20  
- File B: Rahul age = 22  

😱 Which one is correct?

**Redundancy → causes → Inconsistency**

---

## 3️⃣ Difficulty in Accessing Data

Hard to retrieve specific information quickly.

You want:

> "List of students with marks > 90"

In file system you must:

- open file  
- write custom program  
- manually search  

❌ Very slow

---

## 4️⃣ Data Isolation

Data scattered in different files and formats.

**Definition:**  
Data isolation is the difficulty in accessing related data because data is stored in different files and formats.

Student data in:

- student.txt  
- marks.csv  
- attendance.xls  

**Example:**  
"Show students with attendance > 80% and marks > 90"

😵 Very difficult in file system.

---

## 5️⃣ Integrity Problems

Data correctness rules.

**Example rules:**

- Age cannot be negative  
- Marks must be ≤ 100  
- Account balance ≥ 0  

---

## 6️⃣ Atomicity Problem

Transaction should happen fully or not at all.

---

## 7️⃣ Concurrent Access Problems

When many users access and update same data simultaneously → conflicts occur.

---

# ✅ DBMS Provides

- centralized control  
- SQL queries  
- concurrency control  
- transactions (ACID)  
- integrity constraints  
- better security  
- reduced redundancy  

---

# 👨‍💼 DBA (Database Administrator)

**Who manages the database server?**  
👉 That person = DBA

## DBA Responsibilities

- database installation  
- schema design  
- indexing  
- user permissions  
- backup & restore  
- performance tuning  

---

# 🏗️ Why DBMS Architecture Exists

They provide abstraction (hide unwanted details).

✅ EXACTLY RIGHT.

## 🎯 Goal of Architecture

- Hide storage complexity  
- Show only needed data  
- Make system easy to use  

👉 This is called **Data Abstraction**

---

# 🧠 Three-Schema Architecture (Core Concept)

Every DBMS (MySQL, MongoDB, Oracle…) conceptually follows 3 levels.

⚠️ **Important:**

- Concept is same  
- Implementation is different  

---

## Level 1: Physical Level (Internal Level)

✅ What it describes:

👉 HOW data is stored inside disk

**Examples:**

- indexing  
- hashing  
- B+ trees  

---

## Level 2: Logical Level (Conceptual Level) ⭐ MOST IMPORTANT

Logical level identifies what data is stored.

Logical level exists in BOTH MySQL and MongoDB but representation differs:

- MySQL → tables  
- MongoDB → collections/documents  

---

## Level 3: View Level (External Level)

👉 What each user sees  
👉 user-specific view  
👉 hides rest of data  

User writes query and sees data.

---

## 👨‍💻 Where Developers Work

**Answer:**

👉 Mostly Logical level  
👉 and View level  

---

# 📐 Schema vs Instance

Schema is the blueprint of the database, whereas instance is the actual data at a particular time.

---

# 📊 Data Model

Data model is a way to describe the structure of a database.

**Types:**

- ER model (graphical)  
- Relational model  
- Document model (MongoDB)  

---

# 🔧 DBA Main Duties

### 1️⃣ Define schema
Creates tables/collections.

### 2️⃣ Manage storage

Includes:

- where files stored  
- indexing  
- performance tuning  
- memory allocation  

👉 Not manual file browsing — system level control.

### 3️⃣ Control access

- who can read  
- who can write  
- roles and permissions  

### 4️⃣ Backup & recovery

If system crashes → DBA restores database from backup.

### 5️⃣ Security

- encryption  
- user authentication  
- authorization  

---

# 🏛️ Application Architecture

Application architecture = How app + DB are arranged.

It describes:

- where client is  
- where server is  
- where database is  

---

## 🖥️ 1-Tier Architecture

### ✅ Structure

Everything in one machine.

User + App + Database (all in same system)

**Example:**

- MS Access  
- SQLite local app  

### ❌ Problems

- not scalable  
- not secure  
- single user mostly  

---

## 🏗️ 2-Tier Architecture

### ✅ Structure

Client (App) ↔ Database Server

**Example:**

- Java desktop app + MySQL  
- .NET app + SQL Server  

### ⚠️ Limitation

- business logic in client  
- harder to scale  

---

## ⭐ 3-Tier Architecture (MOST IMPORTANT)

Used by modern web apps (including MERN).

### ✅ Structure
Client (React)
↓
Application Server (Node/Express)
↓
Database Server (MongoDB/MySQL)


---

# 📈 What is Scalability?

System can handle more users without crashing.

If 100 users → works  
If 10,000 users → still works  

👉 That system is scalable

**Types**

- vertical scaling (bigger machine)  
- horizontal scaling (more servers)  

---

# 🧠 Data Model (ER Model)

ER model represents the real world using:

- entities  
- attributes  
- relationships  

ER model is a high-level conceptual data model that represents real-world objects as entities and their relationships.

---

## 🔹 Entity

Entity = real-world object that is distinguishable.  
An entity is a real-world object that can be uniquely identified.

---

## 🔹 Strong Entity

- Can be uniquely identified by its own attributes  
- Has primary key  
- Exists independently  

---

## 🔹 Weak Entity

- Cannot be uniquely identified alone  
- Depends on strong entity  

**Classic Example:**

Loan → Strong  
Payment → Weak  

Why? Payment number repeats for each loan.

---

## 🔹 Entity Set

Collection of similar entities having the same attributes.

**Examples:**

- Student  
- Customer  
- Employee  

---

## 🔹 Attributes

Attributes = properties of entity.

**Example (Student):**

- Student_ID  
- Name  
- Age  
- Phone  

---

## 🔹 Relationship

Relationship = connection between entities.

---

# 🔢 Degree of Relationship

### Unary
One entity related to itself.  
Example: Employee manages Employee

### Binary ⭐ MOST COMMON
Two entities.  
Example: Student takes Course  
🔥 90% cases are binary

### Ternary
Three entities.  
Example: Employee works_on Project at Location

---

# 🔗 Cardinality

### One-to-One (1:1)
One A ↔ One B  
Example: Citizen ↔ Aadhaar

### One-to-Many (1:N)
One A → many B  
Example: One customer → many orders

### Many-to-One (N:1)
Many A → one B  
Example: Many students → one department

### Many-to-Many (M:N) ⭐ MOST IMPORTANT
Many A ↔ many B  
Example: Students ↔ Courses

---

# 🔒 Participation Constraint

## Total Participation
Every entity must participate.  
Example: Loan must belong to customer.

## Partial Participation
Participation optional.  
Example: Customer may or may not take loan.

---

# 🔍 Strong vs Weak Entity (How to Identify)

**Golden Rule:**

- YES → Strong entity  
- NO → Weak entity  

---

# ✏️ ER Diagram Drawing Steps

1. Find Entities  
2. Find Attributes  
3. Find Primary Keys  
4. Find Relationships  
5. Find Cardinality  
6. Find Participation  
7. Check Weak Entities  

---

# 🚀 Extended ER (EER)

Normal ER is good for basic modeling.  
Real-world systems are complex → use EER.

## 🔥 Main EER Features

- Specialization  
- Generalization  
- Inheritance  
- Aggregation  

### Specialization
Process of dividing a higher-level entity into lower-level sub-entities.

### Generalization
Process of combining similar entities into a higher-level entity.

### Inheritance
Subclass entities inherit attributes of the superclass.

---

## 🔷 Aggregation

Used when we need relationship ↔ relationship.

Aggregation is an abstraction technique used to treat a relationship as a higher-level entity.

---

# 🗄️ Relational Model

Relational Model represents data in the form of relations (tables).

- Relation = Table  
- Tuple = one row (one record)  
- Domain = set of allowed values for an attribute  

Relational schema = structure/design of a relation.  
Relation instance = actual data stored in the table at a particular time.

---

# 🔑 Keys

## Super Key
Any set of attributes that uniquely identifies a tuple.

✔️ may contain extra attributes  
✔️ may be many  

## Candidate Key
Minimal super key (no redundant attribute).

⚠️ Candidate key values should be UNIQUE and NOT NULL.

## Primary Key
One candidate key chosen to uniquely identify tuples.

✔️ only one primary key per table  
✔️ unique + not null  

## Alternate Key
Candidate keys not chosen as primary key.

## Composite Key
Primary key made of more than one attribute.

## Surrogate Key
Artificial key generated by DBMS with no business meaning.

**Examples:**

- AUTO_INCREMENT id  
- UUID  

---

# 🛡️ Integrity Constraints

Integrity ensures data remains accurate and consistent.

## Domain Constraint
Attribute values must come from valid domain.

## Entity Integrity Constraint
Primary key must be UNIQUE and NOT NULL.

## Referential Integrity Constraint
Foreign key must either be NULL or match parent primary key.

---

## Delete Cases

**NO ACTION / RESTRICT (default)**  
❌ Cannot delete parent if child exists

**ON DELETE CASCADE**  
✅ Parent deleted  
✅ Child rows automatically deleted

**ON DELETE SET NULL**  
✅ Parent deleted  
✅ Child FK becomes NULL

---

# 🔄 ER to Relational Mapping Rules

- Strong entities  
- Weak entities  
- Relationships  
- Multivalued attributes  
- Composite attributes  
- Generalization  
- Aggregation  

---

## RULE 1: Strong Entity → Table

- Strong entity becomes its own table  
- Attributes → columns  
- Primary key stays primary key  

---

## RULE 2: Weak Entity → Table ⭐ VERY IMPORTANT

Include:

1. Its own attributes  
2. Owner’s PK as FK  
3. Composite PK = (Owner PK + partial key)

---

## RULE 3: Single-Valued Attribute

👉 Just make it a column.

---

## RULE 4: Composite Attribute

👉 Break into parts  
👉 Ignore main composite name

---

## RULE 5: Multivalued Attribute

👉 Create NEW table

---

## RULE 6: Derived Attribute

👉 DO NOT store in table  
Because it can be calculated.

---

## RULE 7: Generalization (EER → Tables)

### 🌟 Method 1 (MOST COMMON & SAFE)

Create:

- one table for superclass  
- one table for each subclass  

### Method 2 (special case only)

Use only when:

- disjoint  
- total specialization  

👉 For interviews, Method 1 is enough.

---

## RULE 8: Aggregation

👉 Treat relationship as table  
👉 Include PKs of participating entities  
👉 Add relationship attributes  

---


**Functional Dependency (FD)**

---

A functional dependency  
𝐴→𝐵  
A→B means:

If two rows have the same value of A, they must have the same value of B.

A = determinant  
B = dependent  
FD is the tool to detect and remove redundancy.

If I know column A, can I uniquely find column B in the real world?”

If YES → FD exists.
Example 1:
| StudentID | StudentName |
If I know StudentID, can I uniquely know StudentName?
Yes → StudentID → StudentName

Example 2:
| StudentName | Dept |
If I know StudentName, can I uniquely know Dept?
Not always (two Ravi may exist)
So no FD.
---

Redundancy happens when we store an attribute in a table where its determinant is not the key.

This is the heart of normalization.
---
**Types of Functional Dependency**

---

**1️⃣ Trivial FD**

**Rule:**

𝐴 → 𝐵 is trivial if 𝐵 ⊆ 𝐴  
A→B is trivial if B ⊆ A

✅ **Example:**

{EmpID, Name} → EmpID  

Because EmpID is already part of left side

---

**Non-Trivial FD**

**Rule:**

𝐴 → 𝐵 is non-trivial if 𝐵 ⊄ 𝐴  
A→B is non-trivial if B ⊄ A

✅ **Example:**

EmpID → Name

---

**Normalization**

---

**Main goal:**

Reduce redundancy and remove anomalies.

**Three anomalies:**

- Insertion anomaly  
- Deletion anomaly  
- Update anomaly  

---

**Normal Forms**

---

**First Normal Form (1NF)**

✔ **Rule:**

- No multivalued attributes  
- Each cell must be atomic (single value)  
- No repeating groups  

✅ **Example violation:**

Student Phones  
A → 999,888  

✔ **Fix →** split rows or new table.

---

**Second Normal Form (2NF)**
When to check?

👉 Only when composite key exists.
✔ **Preconditions:**

- Must already be in 1NF  

✔ **Rule:**

No partial dependency

**Meaning:**

Every non-prime attribute must depend on the whole primary key, not part of it.

---

**Third Normal Form (3NF)**

You were close but slightly messy. Here's the clean rule.

✔ **Preconditions:**

- Must be in 2NF  

✔ **Rule:**

No transitive dependency of non-prime attributes on key.

**Formally:**

For every FD 𝐴 → 𝐵:

At least one must be true:

- A is superkey, OR  
- B is prime attribute  

---

✅ **Transitive dependency**

𝐴 → 𝐵, 𝐵 → 𝐶  
Then:  
𝐴 → 𝐶  

If B and C are non-prime → violates 3NF.

---

**BCNF Rule (VERY IMPORTANT)**

---

For every functional dependency:

𝐴 → 𝐵  

A must be a superkey

---

**Why BCNF is stronger than 3NF**

3NF allows some cases where determinant is not superkey.

---

**Classic example (important)**

Relation:

(Student, Course, Instructor)

FDs:

(Student, Course) → Instructor  
Instructor → Course ❌  

Here:

- Instructor is not superkey  
- But determines Course  

👉 violates BCNF  
👉 may still satisfy 3NF  

| Student | Subject | Teacher |
| ------- | ------- | ------- |
| Ravi    | DBMS    | Smith   |
| Priya   | DBMS    | Smith   |
| Ravi    | OS      | John    |

Try Teacher alone

Look at Teacher = Smith.

Rows:

Student	Subject	Teacher
Ravi	DBMS	Smith
Priya	DBMS	Smith

👉 Same teacher appears in multiple rows.

🚨 So Teacher alone CANNOT uniquely identify a row.

Therefore:

❌ Teacher is NOT a super key.
Try (Student, Teacher):

| Student | Teacher | → unique row? |

Check:

Ravi + Smith → one row

Priya + Smith → different row

✅ Works.

So candidate key = (Student, Teacher)

---



**What is a Transaction?**

---

A transaction is a logical unit of work that consists of one or more database operations and must be executed completely or not at all.

---

**Example (Money Transfer — BEST)**

---

Suppose person A transfers ₹100 to person B.

**Transaction steps:**

- Read A balance  
- Deduct ₹100 from A  
- Write A balance  
- Read B balance  
- Add ₹100 to B  
- Write B balance  

👉 All these steps together form one transaction.

If any step fails → entire transaction must be undone.

---

**ACID Properties**

---

**A — Atomicity (All or Nothing)**

**Meaning:**

Either the entire transaction executes or none of it executes.

✅ No partial updates allowed.  
If any part of the transaction fails, the DBMS performs a rollback to undo all previous operations.

**Example**

If system crashes after deducting money from A but before adding to B:

❌ WRONG state  
✅ DBMS must rollback A’s deduction.

---

**C — Consistency (Valid → Valid)**

After a transaction, the database must remain in a valid state satisfying all constraints.

💡 **Example**

Suppose rule:

Total money in system must remain constant.

**Before transfer:**

- A = 1000  
- B = 2000  
- Total = 3000  

**After transfer:**

- A = 900  
- B = 2100  
- Total = 3000 ✅ valid state  

If total becomes 2900 ❌ → consistency violated.

🎯 **Interview one-liner**

Consistency ensures the database moves from one valid state to another valid state.

---

**I — Isolation**

Concurrent transactions should not interfere with each other’s intermediate states.

**Your GPay example (refined)**

Two transactions start:

- T1 (GPay)  
- T2 (Net banking)  

Both read balance = 1000.

If isolation is weak:

- Both deduct 100  
- Final balance becomes wrong  

Each transaction behaves as if it is running alone.

DBMS uses:

- locks  

Isolation ensures that concurrent transactions execute without affecting each other’s intermediate results.

---

**D — Durability**

Once a transaction is committed, its changes are permanently stored even if the system crashes.

Once the transaction is committed, even if the system crashes, the changes must persist.

**Example**

User gets message:

✅ "Payment successful"

Immediately system crashes.

After restart → money must still be transferred.

---

**Transaction States (Clean Flow)**

---

🔹 **1. Active**

- Transaction is executing  
- Read/write happening  

---

🔹 **2. Partially Committed**

- Last statement executed  
- Commit not yet fully guaranteed  
- Still vulnerable  

---

🔹 **3. Committed**

- All changes permanently recorded  
- Success  

---

🔹 **4. Failed**

- Error occurred  
- Cannot proceed  

---

🔹 **5. Aborted**

- All changes rolled back  
- Database restored to previous state  

---

🔹 **6. Terminated**

- Transaction leaves the system  
- Final state (after commit or abort)
