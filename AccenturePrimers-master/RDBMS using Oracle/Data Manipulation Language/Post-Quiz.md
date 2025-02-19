# Post Quiz

1. Which are auto-commit statements?
    - Drop, Truncate
2. Which of the update statement produces the following error in the employee table?
ORA-02291: integrity constraint (SYS_C23) violated - parent key not found.
    - UPDATE Employee SET Deptid=3 WHERE Empid = 101;

3. Which of the following is not a DML statement?
    - DROP, ALTER
4. Which SQL statement needs both insert and update privilege on the target table and select privilege on the source table?
    - merge
5. On delete restrict is used to restrict the deletion of child records. State True or False.
    - True
6. Delete statement supports up to two conditions only. State True or False
    - False
7. Which statement inserts a new row into the STUDENT table?
    -  INSERT INTO student (stud_id, address, name, dob)
VALUES (101,'100 Main Street','Smith','17-JUN-99');
8. insert into employee(empid,empname)values(123,'John');

When we issue the above insert command and if the statement fails,

what would be the reason.

    - Value for phoneno is missing.
9. DELETE FROM dept WHERE dept_id = 901;
The above delete statement throws an integrity constraint error because a child record was found. What could we do to make the statement execute?

    - Delete the child records first.
10. Which query is used to delete employee records whose age is greater than 55?
    - Delete from employee where age >55;

    
