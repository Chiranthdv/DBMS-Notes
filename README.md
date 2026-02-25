# DBMS-Notes
Data = raw facts (unprocessed) .It has no meaning by itself.
Data is a collection of raw, unorganized facts that by itself has no meaning.
Information = processed data that has meaning
Information is processed and organized data that is meaningful and useful for decision-making.
👉 Data = input
👉 Information = output

Data is raw and unprocessed facts, whereas information is processed data that is meaningful and useful.

Database = organized collection of data
A database is an organized collection of related data stored electronically for easy access and management.
Stored so we can:
access easily
update easily
manage easily
Your college system storing:
student details
marks
attendance
👉 That storage = Database
DBMS = software that manages databases
DBMS is software that enables users to efficiently store, retrieve, update, and manage data in a database.
It helps to:
store data
retrieve data
update data
delete data
Examples of DBMS:MySQL,Oracle,PostgreSQL,MongoDB

Disadvantages of File System

1. Data Redundancy-> same data stored multiple times
Student data stored in:
admission.txt
library.txt
hostel.txt
Same student info repeated

Example:
Library needs student data → creates library file
Hostel needs student data → creates hostel file
Result → duplicate data

2. Data Inconsistency-> same data has different values in different files
Example:
File A: Rahul age = 20
File B: Rahul age = 22
😱 Which one is correct?
Redundancy → causes → Inconsistency

3. Difficulty in Accessing Data:Hard to retrieve specific information quickly.
You want:
"List of students with marks > 90"
In file system you must:
open file
write custom program
manually search
❌ Very slow
4. Data Isolation:data scattered in different files and formats.
 Data isolation is the difficulty in accessing related data because data is stored in different files and formats.
Student data in:
student.txt
marks.csv
attendance.xls
Ex: "Show students with attendance > 80% and marks > 90"
😵 Very difficult in file system.
5. Integrity Problems: data correctness rules
 Example rules:
Age cannot be negative
Marks must be ≤ 100
Account balance ≥ 0

6. Atomicity Problem:transaction should happen fully or not at all
7. Concurrent Access Problems:When many users access and update same data simultaneously → conflicts occur.

#  DBMS provides:
✅ centralized control
✅ SQL queries
✅ concurrency control
✅ transactions (ACID)
✅ integrity constraints
✅ better security
✅ reduced redundancy

DBA->
✅ database installation
✅ schema design
✅ indexing
✅ user permissions
✅ backup & restore
✅ performance tuning
Who manages the database server?
That person = DBA
