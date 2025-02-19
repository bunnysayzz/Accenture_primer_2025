# Pre Quiz

1. By using _____ datatype we can store numeric and character values as an input .
    - varchar2, varchar, Char
2. Check constraint can be used for both column level and table level
3. To permanently remove all the data from the STUDENT table, and you need the table structure in the future. Which single command performs this? 
    - TRUNCATE TABLE student; 
4. Which statement would you use to add a primary key constraint to the patient table using the id_number column, immediately enabling the constraint? 
    - ALTER TABLE patient ADD CONSTRAINT pat_id_pk PRIMARY KEY(id_number);
5. Composite key is used in one to one relationship. State true or false.
    - False
6. Which CREATE TABLE statement is valid?
    - CREATE TABLE ord_details (ord_no NUMBER(2), item_no NUMBER(3), ord_date DATE DEFAULT SYSDATE NOT NULL, CONSTRAINT ord_pk PRIMARY KEY (ord_no,item_no));
7. Primary key has a unique and holds the value to identify the record and duplicate null values are not allowed.

8. Cascade constraints are used only in drop statements. State True or False.
    - False
9. A change to the DEFAULT value affects only subsequent insertions to the table.
