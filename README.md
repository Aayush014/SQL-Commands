# Employee DBMS

This repository contains a SQL script to manage an employee database. The database includes basic operations such as adding, updating, retrieving, and deleting employee records.



## Database Schema

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    role VARCHAR(50),
    salary INT,
    age INT,
    phone VARCHAR(20)
);
```

## 1. Adding Employees (Create)

### Add a New Employee

```sql
INSERT INTO employees (id, name, role, salary, age, phone)
VALUES (1, 'Aayush Patel', 'CEO', 7500000, 19, '9879004689');
```

### Add Multiple Employees

```sql
INSERT INTO employees (id, name, role, salary, age)
VALUES 
(2, 'Mann Patel', 'Developer', 80000, 18),
(3, 'Ved Patel', 'Designer', 68000, 17);
```

## 2. Retrieving Employee Information (Read)

### All Employee Information

```sql
SELECT * FROM employees;
```

### Specific Columns for All Employees

```sql
SELECT name, salary FROM employees;
```

### Employees with a Specific Role

```sql
SELECT * FROM employees WHERE role = 'CEO';
```

### Search for Employees by Name

```sql
SELECT * FROM employees WHERE name ILIKE '%ed%';
```

### Employees Older than 30 and Earning More than $70,000

```sql
SELECT * FROM employees WHERE age > 18 AND salary > 70000;
```

## 3. Updating Employee Information (Update)

### Change Salary

```sql
UPDATE employees SET salary = 90000.00 WHERE id = 2;
```

### Update Address

```sql
UPDATE employees SET role = 'Developer & Designer' WHERE role = 'Designer';
```

## 4. Deleting Employees (Delete)

### Remove an Employee by ID

```sql
DELETE FROM employees WHERE id = 2;
```

### Delete Employees by Age

```sql
DELETE FROM employees WHERE age < 18;
```
