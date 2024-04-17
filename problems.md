
1. Insert a new student record with the following details: StudentID: 4, FirstName: 'Emily', LastName: 'Brown', Age: 22, GPA: 3.70.
   ```sql
   INSERT INTO Students (StudentID, FirstName, LastName, Age, GPA)
   VALUES (4, 'Emily', 'Brown', 22, 3.70);
   ```

2. Update the age of the student with StudentID 3 to 20.
   ```sql
   UPDATE Students
   SET Age = 20
   WHERE StudentID = 3;
   ```

3. Delete all students with a GPA below 3.5.
   ```sql
   DELETE FROM Students
   WHERE GPA < 3.5;
   ```

4. Retrieve the first name and last name of all students sorted alphabetically by last name.
   ```sql
   SELECT FirstName, LastName
   FROM Students
   ORDER BY LastName;
   ```

5. Calculate the total number of students in the table.
   ```sql
   SELECT COUNT(*) AS TotalStudents
   FROM Students;
   ```

6. Find the student with the highest GPA.
   ```sql
   SELECT *
   FROM Students
   ORDER BY GPA DESC
   LIMIT 1;
   ```

7. Retrieve the first name, last name, and GPA of the top 3 students with the highest GPAs.
   ```sql
   SELECT FirstName, LastName, GPA
   FROM Students
   ORDER BY GPA DESC
   LIMIT 3;
   ```

8. Calculate the average age of all students.
   ```sql
   SELECT AVG(Age) AS AverageAge
   FROM Students;
   ```

9. Count the number of male and female students in the table.
   ```sql
   SELECT Gender, COUNT(*) AS StudentCount
   FROM Students
   GROUP BY Gender;
   ```

10. Find the student(s) with the lowest GPA.
    ```sql
    SELECT *
    FROM Students
    WHERE GPA = (SELECT MIN(GPA) FROM Students);
    ```

11. Retrieve the first names of customers whose names start with "J".
    ```sql
    SELECT first_name
    FROM Customers 
    WHERE first_name LIKE "J%";
    ```
**ALTER**
1. Add Column
   ```sql
   ALTER TABLE table_name
   ADD COLUMN column_name datatype constraint
   ```

2. Drop Column
   ```sql
   ALTER TABLE table_name
   DROP COLUMN column_name
   ```

3. Rename Table
   ```sql
   ALTER TABLE table_name
   RENAME TO new_table_name
   ```

4. Change Column
  ```sql
  ALTER TABLE table_name
  CHANGE COLUMN old_name new_name new_datatype new_constraint;
  ```

5. Modify Column
   ```sql
   ALTER TABLE table_name
   MODIFY col_name new_datatype new_constraint;
   ```

 

1. **Total number of employees in each department**:
```sql
SELECT department, COUNT(employee_name) AS total_employees
FROM employees
GROUP BY department;
```

2. **Departments with more than two employees**:
```sql
SELECT department, COUNT(employee_name) AS total_employees
FROM employees
GROUP BY department
HAVING COUNT(employee_name) > 2;
```

3. **Average salary of employees in the IT department**:
```sql
SELECT AVG(salary) AS average_salary_it
FROM employees
WHERE department = 'IT';
```

4. **Number of employees with a salary higher than $60,000**:
```sql
SELECT COUNT(*) AS high_salary_count
FROM employees
WHERE salary > 60000;
```

5. **Employee with the highest salary**:
```sql
SELECT employee_name, salary
FROM employees
ORDER BY salary DESC
LIMIT 1;
```

6. **Total salary expense for the company**:
```sql
SELECT SUM(salary) AS total_salary_expense
FROM employees;
```

7. **Department with the highest average salary**:
```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
ORDER BY AVG(salary) DESC
LIMIT 1;
```

8. **Employees in the HR department earning more than the department's average salary**:
```sql
SELECT employee_name, salary
FROM employees
WHERE department = 'HR'
AND salary > (SELECT AVG(salary) FROM employees WHERE department = 'HR');
```

9. **Employees along with their departments, sorted by department name**:
```sql
SELECT employee_name, department
FROM employees
ORDER BY department;
```


