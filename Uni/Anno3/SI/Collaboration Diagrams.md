Describe the interactions between the objects by
organisations. Show how objects interacts with respect to organisational units (see [[Interaction Diagrams#Boundaries]]).
Sequence of messages determined by numbering
- 1, 2, 3, 4, …..
- 1, 1.1, 1.2, 1.3, 2, 2.1, 2.1.1, 2.2, 3
(shows which operation calls which other operation)

![[Pasted image 20251013130846.png]]

### Comparison with Interaction Diagrams
- Sequence diagrams are best to see the flow of time -> sequence of messages more difficult to understand in collaboration diagrams.

- Flow of control by organisation is best seen through collaboration diagrams -> layout of collaboration diagrams may show static connections of objects

- Complex control is difficult to express anyway!!!

### Content
**Objects**:
- they exchange messages among each-other
**Messages**:
- Synchronous: “call events,” denoted by the full arrow
- Asynchronous: “signals,” denoted by a half arrow
- There are also «create» and «destroy» messages
- Messages are numbered and can have loops

Almost same stuff as sequence diagrams!!!!

### Example
![[Pasted image 20251013131306.png]] 