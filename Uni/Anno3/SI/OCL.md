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