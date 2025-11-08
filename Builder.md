This pattern is used to create a complex object while separating its construction process from its representation.

- The building process is delegated to a director of object building.
- The director keeps a list of complex objects to be created and directs the building process to the proper component builder.

Lets us have different implementation/interfaces of an object’s parts, giving finer control over the construction
process.

![[Pasted image 20251108135739.png]]