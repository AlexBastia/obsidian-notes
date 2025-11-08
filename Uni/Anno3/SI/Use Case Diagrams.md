Requirements/ early Analysis. 
A Use Case describes a typical interaction between actors and the system.

For every discrete thing the customer wants to do with the system:
- give it a name
- describe it shortly

The first questions a Use Case should answer are the following:
- What are the main tasks or functions that are performed by the actor?
- What system information will the the actor acquire, produce or change?
- Will the actor have to inform the system about changes in the external environment?
- What information does the actor desire from the system?
- Does the actor wish to be informed about unexpected changes?

Example of the NYSE Use Case:
![[Pasted image 20251007175726.png]]

## Actors
**Actors** are the role that a user plays with respect to the system, although they don't have to be human. They can get value from the use case or participate in it.

## Extends relationship
One use case is similar to another but does a bit more:
- Capture the simpler use case first.
- For every step ask: "What could go wrong?" "How could things work out differently?".
- Plot every variation as an extension to the use case.
![[Pasted image 20251007180254.png]]

## Includes relationship
Used when a chunk of behaviour is similar across different use cases (avoids copy and paste).
![[Pasted image 20251007180413.png]]

### Generalisation
Similar to inheritance in OOP, connects a use case to a more general one.
![[Pasted image 20251029205706.png]]
Here, both buy watch and buy product are valid use cases (they are equally significant), but the former is more specific and can be used whenever buy product is used.
