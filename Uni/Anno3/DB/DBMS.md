A **DataBase Management System** is any system managing data collections that are:
- big
- persistent 
- shared
While ensuring: 
- privacy 
- reliability 
- efficiency 
- effectiveness

There are lots of DBMS's available as products on the market (DB2, Oracle, SQLServer, MySQL,...).

The data could also be managed by a simple **file system**, but these only provide a coarse grained access to data: 'all or nothing'.

### Describing Data
Different levels of abstraction:
- [[Data Model]]: independent from physical representation, used in programs.

### Organizing Data
> **Schema**: time invariant, describes the data's structure (intentional).
> **Instance**: actual values that can change (extensional).

Two different "aspects"(?):
- **Conceptual Models**: used in the preparatory phase of a project (Entity-Relationship). (See [[OO Concept Modelling]] for a more detailed explanation from a software engineering point of view).
- **Logical Models**: used by software at a higher level to organize and store data ([[Relational Model]], lattice, ...)

### Architecture
#### Simplified
![[Pasted image 20251011124605.png]]
**Logical Schema**: describes the structure of the database through the logical data model (e.g., the table’s structure).
**Internal Schema**: represents the logical schema at the storage level using specific raw data structures (such as files, records and data pointers).
	Note: logical data is independent from its internal representation (**Physical Data Independence**), for this reason we will focus solely on the first.

#### ANSI/SPARC
![[Pasted image 20251011124912.png]]
**External schema**: describes part of the database in a logical model using **partial views** and derived tables.
	Note: The external level is independent from the logical level, so edits on "views" don't require any change at the logical level and "transparent" edits at the logical level keep the external schema unaltered (**Logical Data Independence**).

### Languages
Another aspect of the database effectiveness is given by its availability through different languages and interfaces:
- “interactive” textual languages (SQL)
- statements (SQL) injected in a host language (Pascal, Java, C ...)
- statements (SQL) injected in an ad hoc language with other features (e.g., plots, printing tables)
- user friendly interfaces (with no textual interface)

Remember to separate data from software:
- **Data Definition Language** (DDL): used for defining the schemas (logical, external, physical) and other operations.
- **Data Manipulation Language** (DML): query and update (instances of) databases.