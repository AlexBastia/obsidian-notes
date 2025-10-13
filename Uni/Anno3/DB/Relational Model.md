**Value-based** logical model (references between data stored within relations are represented through values).

### Relations and Relationships
- [[Logic Relation]] as in Set Theory
- Relation as in the relational data model
- Relationship expresses a specific class of facts in the Entity-Relationship model

### Definitions
- **Schema of a relation**: a relation $R$ over a set of attributes $A_1,...,A_n$:
$$R(A_1,...,A_n)$$
	STUDENTS(Number, Surname, Name, Year of Birth)

- **Schema of a database**: a set of schemas (itself a relation):
$$R = \{R_1(X_1),...,R_n(X_n)\}$$
	R = {STUDENTS(Number, Surname, Name, Year of Birth), EXAMS(Student, Grade, Lecture), LECTURES(Code, Name, Lecturer)}

- **Tuple** over a set of attributes $X$: a mapping from each attribute $A$ in $X$ to a value in $A$'s domain. $t[A]$ expresses the value of a tuple $t$ over the attribute $A$.
	$t[Name]$ = Mario (if $t$ is the first tuple in STUDENTS)

- **Relation Instance**: a finite set of tuples having schema $R(X)$
	![[Pasted image 20251011140254.png]]

- **Relation Database Instance**: set of relation instances $r=\{r_1,...,r_n\}$ on a database schema $R = \{R_1(X_1),...,R_n(X_n)\}$.
	![[Pasted image 20251011140322.png]]

### Positional vs Non-positional
![[Pasted image 20251011133014.png]]
Each domain (*string*, *int*) appears with two distinct **roles** (home team/away team, home score/away score) distinguished only by the position in the tuple. The structure is **positional**.

![[Pasted image 20251011133230.png]]
An **attribute** is associated to each domain (first row) to provide the role of the domain. So the position of each attribute is irrelevant, making the structure **non-positional**.

### Tables
A table represents a relation if:
- all rows are different
- all columns headers are different
- values within the columns’ are homogeneous

### References
Value-based -> - References between data stored in different relations are represented through values in the tuples.
![[Pasted image 20251011133901.png]]
Pros:
- Independent from the physical data structure that could dynamically change (the same thing could be provided with “high-level” pointers)
- The only data that is stored is the one that is relevant form the software application point of view
- The user and the programmer see the same data
- Data can be easily shared between different environments
- Pointers are directional

### Integrity Constraints
Some database instances, while syntactically correct, may not represent any correct information for the target application:
	![[Pasted image 20251011174009.png]]
	 The student id doesn't exist, 32 isn't a valid grade and cum laude can be yes only if the grade is 30. Also two students can't have the same number.

From this example we can see that two types of constraints exist:
- **Intra-relational** constraints
	- over values (or domain constraint) (32 isn't a valid score)
	- over tuples (if the score isn't 30, laude can't be 'yes')
- **Inter-relational** constraints (non-existent student id)

### Keys and Superkeys
>A set of attributes univocally identifying tuples within a relation.

More formally:
- A superkey is a set $K$ of attributes on $r$, if there are not two distinct tuples $t1$ and $t2$ in r such that $t1[K] = t2[K]$

A key is a minimal superkey of a relation  (that is, it does not contain another superkey).
	![[Pasted image 20251011203443.png]]
	The Number is a key:
	-  is a superkey
    - contains only one attribute, hence it is minimal

Each relation has a superkey that is the set of all the attributes, hence it has at least one key. This is important because it means we can always access each tuple in a relation. 

#### Primary Keys
Attribute(s) used to form a key, doesn't allow for NULL values (pointed out with underline):
![[Pasted image 20251011204012.png]]

#### Foreign Key Constraint
A **referential integrity constraint**, i.e., foreign key (FK), between the attributes $X$ of a relation $R_1$ and another relation $R_2$, enforce the values on $X$ in $R_1$ to appear as values in the primary key of $R_2$.

An attribute $A$ in $R1$ is a foreign key that references the relation $R2$ if it satisfies the following rules:
1. The attribute $A$ has the same domain as the primary key attribute of $R2$
2. A value of $A$ in a tuple $t1$ in $R1$ either is NULL or occurs as a value for some tuple $t2$ in $R2$, such that $t1[A] = t2[PK]$ (a.k.a. $t1[FK] = t2[PK]$)