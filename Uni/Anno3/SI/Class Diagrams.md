Shows static structure of the system, including:
- Types of objects
- Relationships (Association, Subtypes, Dependency)
![[Pasted image 20251007181601.png]]

Classes can be part of several diagrams and only relevant information has to be displayed for each one. 

## Associations
Relationship between classes. Has a *name*, a *direction* and a *multiplicity* and a *role* for each side.
![[Pasted image 20251007182853.png]]
### Roles
Identifies one end of an association. A role name can be implicit or explicit (needed between objects of the same class).

### Responsibilities
![[Pasted image 20251007183640.png]]

### Navigability
![[Pasted image 20251007183725.png]]
In this case:
- The Order has to be able to determine the Customer
- The Customer does not know all Orders
### Association Classes
Useful if the attributes don't belong to any specific class but to the association itself. 
![[Pasted image 20251007183948.png]]

### Aggregation
![[Pasted image 20251008101451.png]]
In this case we're saying that a Company is composed of *many* Units, witch contain *many* Departments and so on.

We're basically showing that the Company class has multiple Unit objects in its attributes **as references.**

### Composition
Similar to aggregation, but in this case components belong only to one whole. When the containing class is deleted, so are all its components.