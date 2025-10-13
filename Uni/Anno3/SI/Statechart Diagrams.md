Describes the evolution of the states of any classifier, commonly used for objects (but can also refer to subsystem etc.)
Shows the behaviour of *one* object:
- how does it change its state based on the messages it
receives
- narrowly focused, fine-grained

## Object States
Set of values that describe an object at a specific moment in time (attribute values)
### State changes
When an event occurs (a message is received), states may change:
![[Pasted image 20251008105230.png]]

## Notation
Two types of method:
- Activity: Can take longer and be interrupted
- Action: Occurs quickly
Main methods:
- entry: an action that is performed on entry to the state
- do: an ongoing activity performed while in the state (example: display window)
- on: an action performed as a result of a specific event
- exit: an action performed on exiting the state
![[Pasted image 20251008105517.png]]

### Sending messages
![[Pasted image 20251008105634.png]]
Guard condition:
- Transition only occurs when guard evaluates to true
- Guards of transitions exiting one state are mutually exclusive


