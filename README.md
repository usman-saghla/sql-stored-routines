# MySQL Stored Routines Practice

This repository contains SQL practice scripts focused on **Stored Procedures** and **Stored Functions** in MySQL.  
The examples are based on the **Employees sample database** and demonstrate reusable SQL logic for tasks like calculating salaries, retrieving employee IDs, and returning specific values from queries.

---

## 📂 Repository Contents

- `Stored_Routines.sql` → Contains all stored routine scripts:
  - Simple procedure (`avg_salary`)
  - Parameterized procedure (`emp_info`)
  - Function returning values (`emp_info`)

---

## 📌 Topics Covered

### 1. Stored Procedure: `avg_salary`

A simple procedure that calculates the **average salary** from the `salaries` table.

```sql
DELIMITER $$
CREATE PROCEDURE avg_salary()
BEGIN
    SELECT AVG(salary) FROM salaries;
END$$
DELIMITER ;

-- Usage
CALL avg_salary;
CALL avg_salary();
CALL employees.avg_salary;
CALL employees.avg_salary();
