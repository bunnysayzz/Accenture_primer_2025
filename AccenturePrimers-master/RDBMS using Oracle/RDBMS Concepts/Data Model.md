# Data Models

It is a logical representation, which defines structures or the way to store records in DBMS.

How records are stored in DBMS ? 

It depends on supported Data Model. 

## Descripton of Relationship
It provides the description of how records are related to each other, what are constraints and how data is accessed.

## Aspect select the Data Model

DBMS has to select the proper data model by considering 3 critical aspects.

1. Structure - how the data is going to be stored.
2. Operations - performed on the data.
3. Constraints


## Hierarchical Data Model

* Developed by IBM in 1960s and used in earyly mainframe DBMS.


1. What Structure does it follow ?
    - Tree
2. How records are stored ?
    - Node
3. Can root or parent node have many children ?
    - Yes
4. Can Child nodes have many parents ?
    - No
5. Can you search the data on the child node easily ?
    - No, every search should start from root.


## Network Data Model 

Network model was invented by Charles Bechman, developed and published in 1970.

1. What Structure does it follow ?
    - Graph
2. How records are Stored ?
    - Node
3. Can root or parent node have many children ?
    - Yes, chlid node can have many parent nodes.
4. Can you search the data on the child node easily ?
    - No, every search should start from root.

## Relational Data Model 

E.F. Codd proposed the relational Model to model data in the form of relations or tables.

1. What Stucture does it follow ?
    - Table
2. How are records stored ?
    - Rows and columns
3. Can root or parent node have many children ?
    - Yes
4. Can you search the data on the child node easily ?
    - Yes, by accessing the relation directly.


### Terminology used in Relational Data Model

1. Degree - number of columns
2. Cardinality - number of rows
3. Attributes refers to the columns of table.

Collection of logically related table stored in database.


# Normalization

Process of dividing the larger table into smaller tables and links them using relationships.

Identifies the keys in each relation to find unique records and make relationship between relations.

This technique helps to organize the tables in a manner that reduces the redundancy and dependancy of data.

It has to follow these normal forms

* First Normal Form
* Second Normal Form
* Third Normal Form

## First Normal Form

Eliminate repeated group of records and move them into a seperate relation.

## Second Normal Form

Eliminate partial dependencies on keys i.e. eliminate the columns that depend only on one part of the key and make a seperate relation.

## Third Normal Form

Eliminate Transitive dependencies on columns that don't depend on the key at all and make a seperate relatoin.