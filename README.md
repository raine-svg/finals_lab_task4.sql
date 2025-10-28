# 📘 Finals Lab Task 4
### Transforming ER Model to Relational Tables  
**Student:** Loraine Alonzo  
**Section:** BSIT 3C  

---

## 🧩 Description  
This project converts an **ER diagram of a student assignment submission system** into **MySQL relational tables**.  
It includes the creation of `student`, `assignment`, and `submission` tables with **primary keys**, **foreign keys**, and **referential integrity constraints**.

---

## 🗂️ Files Included  
- **finals_lab_task4.sql** → SQL script for creating tables and inserting sample data  
- (Optional) **EER Diagram (PDF/JPG)** → Exported from MySQL Workbench  

---

## 🧱 Table Structures  

### 1. student  
| Column | Type | Key |
|---------|------|-----|
| username | VARCHAR(50) | Primary Key |

### 2. assignment  
| Column | Type | Key |
|---------|------|-----|
| shortname | VARCHAR(50) | Primary Key |
| due_date | DATE | Not Null |
| url | VARCHAR(255) | Nullable |

### 3. submission  
| Column | Type | Key |
|---------|------|-----|
| username | VARCHAR(50) | Foreign Key (student.username) |
| shortname | VARCHAR(50) | Foreign Key (assignment.shortname) |
| version | INT | Part of Primary Key |
| submit_date | DATE | Not Null |
| data | TEXT | Submission content |

**Primary Key (submission):** `(username, shortname, version)`

---

## ⚙️ How to Run  
1. Open any MySQL or online SQL compiler (like [sqliteonline.com](https://sqliteonline.com/)).  
2. Copy and paste the code from `finals_lab_task4.sql`.  
3. Run all commands to create tables and insert sample data.  
4. Test with:  
   ```sql
   SELECT * FROM student;
   SELECT * FROM assignment;
   SELECT * FROM submission;
   ```

---

## ✅ Output  
- Tables created successfully  
- Data inserted correctly  
- Referential integrity enforced  

---
