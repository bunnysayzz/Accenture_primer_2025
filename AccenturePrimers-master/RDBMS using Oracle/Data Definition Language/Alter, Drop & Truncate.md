# Alter, Truncate and Drop Statements

**Syntax**

```
ALTER TABLE TableName ADD
(
    ColumnName1 DataType [[CONSTRAINT ConstraintName1] ConstraintType],
    [[CONSTRAINT ConstraintName2] ConstraintType (Cname1 [, Cname2, ...])]
    ........................................................................
    ColumnNameN DataType [[CONSTRAINT ConstraintName1] ConstraintType],
);
```


```
ALTER TABLE Employees ADD Phno NUMBER(8) CONSTRAINT Uk_PhNo UNIQUE;

ALTER TABLE Employees ADD DeptNo NUMBER(3) REFERENCES Department(DepartmentNo);

ALTER TABLE Employeees ADD CONSTRAINT PK_Emp Primary Key(EmployeeNo);

ALTER TABLE Employees ADD CHECK(Salary>0);

ALTER TABLE Employees ADD Unique(Email);

ALTER TABLE Employees MODIFY Name VARCHAR2(15) NOT NULL;

ALTER TABLE Employees ADD unique (Email);

ALTER TABLE Employees ADD PhNo NUMBER(8) CONSTRAINT UK_PhNo UNIQUE;

ALTER TABLE Employees ADD DeptNo NUMBER(3) REFERENCES Department(DepartmentNo);

ALTER TABLE Employeees ADD CONSTRAINT PK_EMP Primary Key(EmployeeNo);
```


## Resize a column 

**Syntax**

ALTER TABLE table_name MODIFY ColumnName New|OldDataType(New|old size) [NOT NULL];

**Example**

ALTER TABLE Department MODIFY NAME VARCHAR2(20);



## Drop column


**Syntax**

ALTER TABLE table_name DROP COLUMN ColumnName;

**Example**

ALTER TABLE Department DROP COLUMN Location;

## Drop Constraint

**Syntax**

ALTER TABLE TableName DROP CONSTRAINT ConstriantName;

**Example**

ALTER TABLE Employees DROP CONSTRAINT UK_PhNo;

## Constrint Name - Predefined & User Defined

Oracle provides a name to each constraint if its not defined by the users.


> Constraint name starts as 'SYS_C' when its defined by oracle.


Oracle maintains a collection of predefined tables to store meta data about database objects created by the users.


The meta data is called data dictionary which has information like 
    - Table Name
    - Owner of the Table 
    - Column Name 
    - Data type
    - Constraint Type

Users has to access these details to know the predefined name of the constaints given by Oracle.


## Disabling a Constraint 

**Syntax**

ALTER TABLE TableName DISABLE CONSTRAINT ConstaintName;


**Example**

ALTER TABLE Employees DISABLE CONSTRAINT PK_Emp;


## Enabling a Constraint 

**Syntax**

ALTER TABLE TableName ENABLE CONSTRAINT ConstaintName;


**Example**

ALTER TABLE Employees ENABLE CONSTRAINT PK_Emp;


> Ensure all the data in the present in the Column should satisfy in the constraint which needs to be enabled.


## Renaming a column 

**Syntax**


ALTER TABLE TableName RENAME COLUMN OldColumnName TO NewColumnName;

**Example**

ALTER TABLE Employees RENAME COLUMN PhNo TO PhoneNumber;



# Rename Table

**Syntax**

RENAME OldTableName TO NewTableName;

**Example**

RENAME Employees TO Employee;


# Truncating a Table


**Syntax**

TRUNCATE TABLE TableName;


> Oracle gives error when try to truncate records in parent tables 'Unique/Primary keys in the table referenced by enabled foreign keys';



# Dropping a Table


**Syntax**

DROP ObjectType ObjectName;

**Example**


DROP TABLE TableName;

