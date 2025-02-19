# Pre Quiz

1. You need to remove all the data from the employee table while leaving the table definition intact. You want to be able to undo this operation. How would you accomplish this task? 
    - DELETE FROM employee; 
2. Which option is used to delete data from both parent and child tables?
    - Cascade
3. How do we represent comments in oracle?
    - /* */ and --
4. Which query will change the cust_address to 'Panama' for those who are from ‘Los Angeles’?
    - Update customer set cust_address=’Panama’ where cust_address=’Los Angeles’;
5. Which statement is used to update multiple rows in a single query?
    - None of the given options : AND WHERE WHEN
6. A DML statement is used to modify the structure of the database. State True or false.
    - False
7. Which statements are true regarding constraints? 
    - A columns with the UNIQUE constraint can contain NULL values.
    - A constraint can be disabled even if the constraint column contains data.

8. Which query will delete all the data in the Employee table that belongs to the employee id 1207?
    - Delete from Employee where emp_id=1207;

9. Create table subjects(Sub_id number(2) primary key,Subj_name varchar(50));
Insert into subjects values (null,’Oracle’);
What will be the output of the given query?

    - The query will generate an ORA-01400: cannot insert NULL value into primary key

10. Which statement is true when a DROP TABLE command is executed on a table? 
    - The table structure and its deleted data cannot be rolled back and restored once the DROP TABLE command is executed. 





