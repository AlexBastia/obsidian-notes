![[Pasted image 20251013131449.png]]

### Breaking a system into subsystems
Different ways:
- Roman principle: Divide & conquer
    - Split up a large system into manageable parts
- Structured methods: functional decomposition
- OO: Group classes into higher level units (Packages / Components)

### Packages
- Show packages.
- Show dependencies between packages. Dependency exists between 2 elements if changes to the definition of one element may cause changes to the other.
- Goal (& art) of large scale design: Minimise dependencies
- Constraints effects of changes
![[Pasted image 20251013131743.png]]

#### Nested packages
![[Pasted image 20251013131826.png]]
2 interpretations
- **transparent**: all contents of contained packages visible
- **opaque**: only classes of the container are visible

#### Restricting package interface complexity
 - Give all classes in the package only package visibility
- Define a public class that provides the public behaviour of the package
- Delegate the public operations to the appropriate class inside the package (Facades)

#### Packages vs Diagrams
**Packages** represent physical divisions of the development to do
 - Their goal is to ease the definition of work packages and to develop software systems
**Diagrams** represent logical assembly of information
- Their goal is ease the understanding of the target domain