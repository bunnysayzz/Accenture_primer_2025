# Post-Quiz

1. Which statement is used to manipulate data without affecting the data in the table?
    - Select
2. DML is used to Manipulate the data stored in a database.
3. Which operator is equivalent to the ‘or’ operator?
    - **In**
4. How to retrieve department_id column without any duplication from employee relation?
    - select distinct department_id from employee;
5. Select the suitable option for retrieving all the employees whose name ends with "kumar"?
    - select * from employee where empname like '%kumar';
6. Select the suitable option for retrieving all the employees whose salary range is between 40000 and 100000?
    - select name,salary from employee where salary>=40000 and salary<=100000;
    - select name,salary from employee where salary between 40000 and 100000;
7. Which statement about SQL is true?
    - Null values are displayed last in ascending sequences.
8. Select the suitable option for retrieving all the employees who have a manager?
    - select empname, manager_id from employee where manager_id is NOT NULL;
9. Which statement is true regarding distinct keywords?
    - Distinct remove duplicate values in the Select clause.