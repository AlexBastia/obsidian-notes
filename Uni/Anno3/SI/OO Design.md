Issues faced in the design of a system:
- *decomposability*—the facility with which a design method helps the designer to decompose a large problem into sub-problems that are easier to solve;  
- *composability*—the degree to which a design method ensures that program components (modules), once designed and built, can be reused to create other systems;  
- *understandability*—the ease with which a program component can be understood without reference to other information or other modules;  
- *continuity*—the ability to make small changes in a program and have these changes manifest themselves with corresponding changes in just one or a very few modules;  
- *protection*—a architectural characteristic that will reduce the propagation of side affects if an error does occur in a given module.

## Main Components
- *Problem domain*—the subsystems that are responsible for implementing customer requirements directly;  
- *Human interaction*—the subsystems that implement the user interface (this included reusable GUI subsystems);  
- *Task Management*—the subsystems that are responsible for controlling and coordinating concurrent tasks that may be packaged within a subsystem or among different subsystems;  
- *Data management*—the subsystem that is responsible for the storage and retrieval of objects.

## From OOA to OOD
![[Pasted image 20251008103957.png]]

In OOD the level of detail is greater, in fact:
-  Names are fixed
-  Fixed signatures for messages
- Multiplicity & its realization
- Visibility
- Algorithms for methods
- More detailed sequence/collaboration diagrams

We still have [[Class Diagrams]] (same structure as OOA), but they're refined to match the design of the system. In addition, we have several new types of diagrams:
- Structural Diagrams: Object Diagrams (deals with instances of classes, homomorphic to Class Diagrams), Deployment Diagrams
- Behavioural Diagrams: [[Sequence Diagrams]], [[Collaboration Diagrams]], [[Statechart Diagrams]], [[Activity Diagrams]]

