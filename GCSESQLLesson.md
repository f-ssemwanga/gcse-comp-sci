# GCSE Computer Science - SQL (Structured Query Language)

 **Learning Objectives**
- Understand SQL commands: SELECT, INSERT, UPDATE, DELETE  
- Write SQL queries to retrieve data from databases  
- Use WHERE clauses and ORDER BY statements  
- Apply SQL knowledge using SQLite DB Browser  

---

##  Concept 1: What is SQL?
SQL (Structured Query Language) is a programming language used to communicate with databases. SQL is a programming language that is used to manipulate information within a database.

**Key SQL Commands (AQA Spec Required):**
- **SELECT** - retrieve data from tables
- **INSERT** - add new records to tables
- **UPDATE** - change existing data
- **DELETE** - remove records from tables

---

##  Task 1: SQLZoo Practice - SELECT Basics
Go to [**SQLZoo Tutorial 0**](https://sqlzoo.net/wiki/SQL_Tutorial)  
Complete exercises 1-3 to understand:

```sql
SELECT population FROM world WHERE name = 'Germany'
```

 **Check**: Can you write a SELECT statement to find specific data?

---

##  Concept 2: SELECT Statement Structure
A SELECT statement comes in four main parts:

```sql
SELECT    -- What information you want
FROM      -- Which table contains the information  
WHERE     -- Criteria to filter the data
ORDER BY  -- How to sort the results
```

**Example:**
```sql
SELECT Forename, Lastname
FROM Students  
WHERE StudentID < 10
ORDER BY Lastname ASC
```

---

##  Task 2: SQLZoo Practice - SELECT with WHERE
Go to **SQLZoo Tutorial 1**  
Practice exercises 1-5 focusing on:
- Using WHERE clauses  
- Filtering data with conditions  
- Using LIKE for pattern matching  

 **Check**: Can you filter data using WHERE conditions?

---

##  Concept 3: ORDER BY and Sorting
`ORDER BY` organizes retrieved data:

- **ASC** = Ascending order (A-Z, 1-10)  
- **DESC** = Descending order (Z-A, 10-1)  

```sql
SELECT * FROM Students 
ORDER BY Lastname, Forename ASC
```

Multiple field sorting: data is first organized by TutorGroup and then by Lastname within each tutor group.

---

##  Task 3: SQLZoo Practice - Ordering Data
Continue with **SQLZoo Tutorial 1** - Focus on exercises that use ORDER BY.  
Try sorting by:
- Single fields  
- Multiple fields  
- Different directions (ASC/DESC)  

 **Check**: Can you sort query results in different ways?

---

##  Concept 4: INSERT Statement
In order to add information into a table within a database using SQL, an INSERT statement is used.

**Structure:**
```sql
INSERT INTO table_name (field1, field2, field3)
VALUES (value1, value2, value3)
```

**Example:**
```sql
INSERT INTO Students (Lastname, Forename, TutorGroup)
VALUES ('Smith', 'Bob', '10RB')
```

Note: Use quotes for text/string data.

---

##  Concept 5: UPDATE Statement
In order to edit or update information within a database using SQL, an UPDATE statement is used.

**Structure:**
```sql
UPDATE table_name
SET field1 = value1, field2 = value2
WHERE condition
```

**Example:**
```sql
UPDATE Students
SET Forename = 'Bob', Lastname = 'Smith'  
WHERE StudentID = 1
```

---

##  Concept 6: DELETE Statement
In order to delete information from a database using SQL, a delete statement is used.

**Structure:**
```sql
DELETE FROM table_name
WHERE condition
```

**Example:**
```sql
DELETE FROM Students
WHERE StudentID = 1
```

 **Warning**: Always use WHERE clause or you'll delete ALL records!

---

##  Task 4: SQLZoo Practice - Advanced SELECT
Go to **SQLZoo Tutorial 2**  
Complete exercises 1-8 practicing:
- Comparison operators (>, <, =)  
- BETWEEN ranges  
- IN lists  
- Pattern matching with LIKE  

 **Check**: Can you use different WHERE conditions effectively?

---

##  Practical: SQLite DB Browser
**Setup**
1. Download: DB Browser for SQLite  
2. Install and open the application  
3. Create New Database: `library_system.db`

**Interface Overview**
- **Database Structure**: View tables and fields  
- **Browse Data**: See table contents  
- **Execute SQL**: Run your SQL commands  
- **DB Schema**: Visual database layout  

---

##  Task 5: Create Your Library Database
Using your schema from Lesson 1, create these tables:

**Books Table:**
```sql
CREATE TABLE Books (
    Book_ID TEXT PRIMARY KEY,
    Title TEXT NOT NULL,
    Author TEXT NOT NULL,
    ISBN TEXT UNIQUE,
    Publication_Year INTEGER,
    Genre TEXT
);
```

**Members Table:**
```sql
CREATE TABLE Members (
    Member_ID TEXT PRIMARY KEY,
    First_Name TEXT NOT NULL,
    Last_Name TEXT NOT NULL,
    Email TEXT UNIQUE NOT NULL,
    Join_Date DATE,
    Member_Type TEXT DEFAULT 'Standard'
);
```
 **Task**: Create these tables in DB Browser (Execute SQL tab)

---

##  Task 6: Insert Sample Data
Add data to your tables:

```sql
INSERT INTO Books (Book_ID, Title, Author, ISBN, Publication_Year, Genre)
VALUES ('BK0001', 'Harry Potter', 'J.K. Rowling', '9780747532699', 1997, 'Fantasy');

INSERT INTO Members (Member_ID, First_Name, Last_Name, Email, Join_Date, Member_Type)
VALUES ('MB0001', 'Emma', 'Smith', 'emma.smith@email.com', '2024-01-15', 'Student');
```

 **Task**:
- Add 2 more books  
- Add 2 more members  
- Check your data in "Browse Data" tab  

---

##  Task 7: Query Your Database
Practice SELECT statements on your data:

```sql
-- Show all books
SELECT * FROM Books;

-- Show only titles and authors  
SELECT Title, Author FROM Books;

-- Find fantasy books
SELECT * FROM Books WHERE Genre = 'Fantasy';

-- Sort members by last name
SELECT * FROM Members ORDER BY Last_Name ASC;
```

**Task**: Write queries to:
- Find all students  
- Show books published after 1980  
- List members by join date (newest first)  

---

##  Task 7: Modify Your Data
Practice UPDATE and DELETE:

```sql
-- Update a member's email
UPDATE Members 
SET Email = 'new.email@school.com'
WHERE Member_ID = 'MB0001';

-- Delete a book
DELETE FROM Books 
WHERE Book_ID = 'BK0001';
```

 **Always use WHERE clause!**  
 **Evidence**: Screenshot before and after your UPDATE and DELETE operations  

---

##  Extension Tasks (Beyond AQA Spec) 
These concepts go beyond the GCSE specification but are valuable for deeper understanding.

**Advanced Queries with JOIN:**
```sql
-- Create Loans table first
CREATE TABLE Loans (
    Loan_ID TEXT PRIMARY KEY,
    Member_ID TEXT NOT NULL,
    Book_ID TEXT NOT NULL,
    Date_Borrowed DATE,
    FOREIGN KEY (Member_ID) REFERENCES Members(Member_ID),
    FOREIGN KEY (Book_ID) REFERENCES Books(Book_ID)
);

-- Query across multiple tables  
SELECT Members.First_Name, Members.Last_Name, Books.Title
FROM Loans
JOIN Members ON Loans.Member_ID = Members.Member_ID  
JOIN Books ON Loans.Book_ID = Books.Book_ID;
```

Note: JOIN queries are A-Level content but useful for understanding relationships.

---

##  Assessment Checklist
 I can:
- Write SELECT statements to retrieve data  
- Use WHERE clauses to filter results  
- Sort data using ORDER BY  
- Insert new records with INSERT INTO  
- Update existing data with UPDATE  
- Delete records safely with DELETE  
- Create simple database tables  
- Use SQLite DB Browser effectively  

## Extension1 (Beyond Spec):  
- Write JOIN queries across multiple tables  
- Understand foreign key relationships  

---

## Extension2
- Complete **SQLZoo Tutorial 3** (Nobel Prize data)  
- Practice SQL: Add 5 more books and 3 more members to your library database  
- Research: Find one real-world example of how SQL databases are used (shopping websites, social media, etc.)  

