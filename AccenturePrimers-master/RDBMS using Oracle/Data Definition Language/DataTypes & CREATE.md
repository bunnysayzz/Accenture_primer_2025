# Datatypes & Create statement

## Data Types

* VARCHAR2(size) - Memory occupied based on number of characters in the input. used to store variable length character data.
    - Eg. "Satya"

* CHAR(size) - Memory occupied is of fixed size which is specified during the creation of columns.
    - Eg. "satya"

* NUMBER(P) - Numeric data, P is precision number of digits
    - Eg. 1234
* NUMBER(P, S) - Floating point numbers
    - P - Total number of digits required including decimal.
    - S - Scale : Total number of digits after decimal.
    - Eg. 768.243, 3.14
* DATE - Date values are in format 'DD-MON-YY'
    - Eg. '25-Aug-24'

> Always use single quotes to specify characters and date values


## CREATE statement
All the db objects are created using 'CREATE' statement of DDL.

**Syntax**

CREATE ObjectType ObjectName(Object Definition);

**Description**

CREATE - Keyword

ObjectType - Table, View, Sequence, Index,...

ObjectName - User Defined name

Object Definition - Detailed structure of the object within ()

; - terminator


**CREATE TABLE syntax**
```
CREATE TABLE TableName
(
    ColumnName1 DataType [[CONSTRAINT ConstaraintName] ContraintType],
    ColumnName2 DataType [[CONSTRAINT ConstaraintName] ContraintType],
    .................................................................
    ColumnNameN DataType [[CONSTRAINT ConstaraintName] ContraintType],
);
```

**Description**

ContraintType - Primary Key, Not Null, Unique, Foreign Key, Check, Default 

1. How to make a relationship between two tables ?

    - Referential Integrity

2. Where is foreign key present ?
    - Child Table

3. Can **any** column be referred from parent table ?

    - No, Only Primary Key and Unique Key columns

4. Can a table have many foriegn keys ?
    - Yes 

5. Can a column be referred from more than one table ?

    - No

6. Can foreign key use any data ?
    - No

7. Should foreign key have unique values ?
    - Not required, can be duplicate, can also be null.

**Foreign Key Syntax**

```
CREATE TABLE TableName
(
    ColumnName1 DataType [[CONSTRAINT ConstaraintName] ContraintType],
    ForeignKeyName DataType [CONSTRAINS ConstraintName] [FOREIGN KEY] REFERENCES parentTableName(ColumnNameFromParent),
    ColumnName2 DataType [[CONSTRAINT ConstaraintName] ContraintType],
    .................................................................
    ColumnNameN DataType [[CONSTRAINT ConstaraintName] ContraintType],
);
```

> DataType same as column referred from parent


> Column name can be differnt but not DataType.

