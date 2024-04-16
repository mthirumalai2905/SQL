
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

