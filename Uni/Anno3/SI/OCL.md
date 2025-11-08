Expression language for [[UML]]
- **pure**, no side effects
- **modelling**, can't be executed
- **formal**, well defined semantics

> **Goal**: to define guard statements in a clean and unambiguous way

### Features
- Same syntax as Java for Attributes (but this becomes self)
- Expressions are strongly type and type conformance is checked
- Operations have assigned pre and post conditions
- Associations of cardinailty 1 are treated as attributes, wheras other associations are treated as sets

UML extension (so it's a modeling language -> can't be executed) that permits the semantic definition of stereotypes. 

Not very used irl.

It's a formal language with well defined semantics, it also doesn't permit side effects.

Expressions are strongly typed -> preconditions and postconditions (assert in C(++))

Associations with cardinality 1 are treated as assignments 

### Goal
Describe guard statements (?) 
