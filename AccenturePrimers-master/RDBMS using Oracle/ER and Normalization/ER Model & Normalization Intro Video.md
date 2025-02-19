# ER Model Concepts

## Entities & Attributes
* Entites
    - are specific objects or things in the real world that are represented in the database.
    - for example EMPLOYEE John Doe, the DEPARTMENT of sales.

* Attributes

    - are properties used to describe an entity
    - for example an EMPLOYEE entity may have a Name, ID, address, Sex, BirthDate.

## Types of Attributes

* Simple :
    - Each entity has a single atomic value for the attribute.
    - EG. Employee ID or Sex.
* Composite:
    - The attribute may be composed of several components.
    - Eg. Address (Door#, Street, City, State, Zip code, Country) or Name (First, Middle, Last)

## Entity Type and Key attributes

Entities with similar attributes are grouped or typed into an entity type.

Eg. Employee entity type, Department entity type.

An attribute of an entity type for which each entity must have a unique value is called a key attribute of the entity type.

Eg. ID of Employee.

### Composite key

A key attribute may be composite (combination of multiple attributes - in such a way that they are unique).

Eg. employeeID is the key of the Employee Entity type with components (DepartmentNumber, EmployeeNumber).


## Relationship and Types

A relationship relates two or more distinct entities with a specific meaning.

Eg. Employee John Doe works in sales Department.

Relationships of same type are grouped or typed into a relationship type.

Eg. WORKS_IN relationship type in which Employees and Departments paerticipate.


## Degree of Relationship

* The degree of the relationship type is the number of participating entity types. Both MANAGES and WORKS_IN are binary relationships.


* More than one relationship type can exist with same participating entity types.

* Eg. MANAGES and WORKS_IN are distinct relationship between EMPLOYEE and Department.

## Structural Constraints on Relations


**Cardinality** (of a binary relationship)

An instance of Entity Type E1 is related with how many instances to Entity E2.


* 1:1 - One to One
* 1:N - One to Many
* M:N - Many to Many

**Optionality** (is the relationship necessary betweent the entities)

* 1 - mandatory
* 0 - optional


