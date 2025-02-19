# Update

* used to change the existing values in the table or in the base table of view or the master table of the materialized view.

* By default, the update statement changes the existing values of a column to all records in the table.

* A WHERE clause is used to limit the updated rows.


* more than one condition can be used in the where clause using LOGICAL OPERATOR like AND OR.

**Syntax**

```
UPDATE TableName
SET 
    Column1 = NewValue1
    [, Column2 = NewValue2, ....., ColumnN = NewValueN]

[WHERE condition];
```

**Example**
```
UPDATE Department
SET 
    location = 'Down Town'
;

UPDATE Department
SET 
    location = 'Down Town'
WHERE DepartmentNo=103;
```

# Delete

* used to delete record(s) from a table, a base table of a view  and the master table of an updated materialized view.


> By defalut delete statement removes all the existing rows from the table.

* A where clause is used to limit the deleted records.

```
DELETE FROM Department;
Output:
Integrity Constraint violated - child records found.
```

> Can we delete the records in parent table if it is referenced in the child table.

* There are three options when the records of the parent table can get deleted
    - `Restrict` : Rejects the delete or update operation of the parent table.
    - `Cascade` : Deletes the row from parent table, and automatically deletes the corresponding rows in the table.
    - `Set Null` : Deletes the row from the parent table, and sets the foreign key value in the child table to NULL.

* These options can be specified while creating foreign keys in the child table by using ON DELETE clause in the CREATE statement.

```
CREATE TABLE TableName
(
    ColumnName1 DataType [[CONSTRAINT ConstraintName] ConstriantType],
    ForeignKeyName Datatype [Constaint ConstraintName] [FOREIGN KEY] REFERENCES ParentTableName(ColumnNameFromParent)
        [ON DELETE reference_option]
    
); 
```

**By Default ON DELETE uses RESTRICT**


> Can the operation performed directly on the parent table ?

* Truncate - No, This option cannot be performed on the parent table.

* Delete - Yes, unless no records from the parent table are referred by the child table, or records which do not have the child records.

> Can the records be reverted after the operation is performed ?

* Trunate - Once the records are removed cannot be reverted.

* Delete - Unless the transaction made a commit.

> Can any particular record alone be deleted ?

* Truncate - No
* Delete - Yes


# MERGE 

* The MERGE statment is used to update or insert records which is selected from one or more sources.
* Conditions are specified to determine wheather to update or insert records into the target table or view.
* It is convinient way to combine multiple operations and is used to avoid multiple INSERT & UPDATEs.
* It cannot update the same row of the target table multiple number of times in the same merge statement.


```
MERGE INTO table_name table_alis 
    USING (table|view|sub_query) alias
    ON (join condition)
WHEN MATCHED THEN
    UPDATE SET 
        col1 = col_val1
WHEN NOT MATCHED INSERT 
    INSERT (column_list)
        VALUES (column_values)
```

**Example**

```
MERGE INTO Employees_OLD EO
USING Employees_UPDATES EU
ON (EO.EMPLOYEENO=EU.EMPLOYEENO)
WHEN MATCHED THEN 
    UPDATE SET EO.SALARY = EU.SALARY
WHEN NOT MATCHED THEN
    INSERT (EMPLOYEENO, NAME, SALARY) 
        VALUES (EU.EMPOLYEENO, EU.NAME, EU.SALARY);
```

