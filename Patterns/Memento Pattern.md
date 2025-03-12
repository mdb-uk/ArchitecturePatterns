[[Architecture Patterns Index]] #SoftwareEngineering #Behavioural
# Memento Pattern

The Memento pattern is a behavioural design pattern that lets you save and restore the previous state of an object without revealing the details of it's implementation.

You could try and copy all the properties etc of an object into some kind of other object, however usually you don't want to expose the inner workings of a class, private members etc, so this would not work. But, if you want to be able to provide some means to roll an object back to a prior state you must find some way around this (other than just making everything public). This is where the memento pattern helps, because it delegates the creation of the snapshot to the originating class itself - which would have access to all private members etc.

The memento object stores these snapshots produced by the originator, looked after by a Caretaker object, and only the object that produced a snapshot has full access to it (to preserve access rights etc). The Caretaker only has limited access to the snapshot metadata, but the originator can roll back it's state with full access to the snapshot if needed.

![[Pasted image 20250106110701.png]]

### References

[Memento](https://refactoring.guru/design-patterns/memento)