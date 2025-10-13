Describe the interactions between objects by time ordering. It focuses on
- objects (and classes)
- message exchange to carry out the scenarios functionality
	The objects are organised in an horizontal line and the events in a vertical time line

### Timeline
![[Pasted image 20251013130047.png]]
Messages point from client to supplier.

### Example
![[Pasted image 20251013130131.png]]

### Content
**Objects**:
- they exchange messages among each-other
**Messages**:
- Synchronous: “call events,” denoted by the full arrow
- Asynchronous: “signals,” denoted by a half arrow
- There are also «create» and «destroy» messages

#### Asynchronous messages
Does not block the caller. Can do 3 things:
- Create a new thread
- Create a new object
- Communicate with a thread that is already running