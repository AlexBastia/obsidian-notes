Used to create an object when the information needed to build it is available only at run time.
- Can be used when a class cannot anticipate the class of the objects it must create.

In this pattern we can create an interface to create an object and let the subclasses decide which class to instantiate.
- This pattern connects parallel class hierarchies.

![[Pasted image 20251108140102.png]]

## Problem
Imagine that you’re creating a logistics management application. The first version of your app can only handle transportation by trucks, so the bulk of your code lives inside the `Truck` class.

After a while, your app becomes pretty popular. Each day you receive dozens of requests from sea transportation companies to incorporate sea logistics into the app.

At present, most of your code is coupled to the `Truck` class. Adding `Ships` into the app would require making changes to the entire codebase. Moreover, if later you decide to add another type of transportation to the app, you will probably need to make all of these changes again.

## Solution
The Factory Method pattern suggests that you replace direct object construction calls (using the `new` operator) with calls to a special _factory_ method.

Now you can override the factory method in a subclass and change the class of products being created by the method.
	There’s a slight limitation though: sub-classes may return different types of products only if these products have a common base class or interface. Also, the factory method in the base class should have its return type declared as this interface.

## Structure
1. The **Product** declares the interface, which is common to all objects that can be produced by the creator and its sub-classes.
2. **Concrete Products** are different implementations of the product interface.
3. 