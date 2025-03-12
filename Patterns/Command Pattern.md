[[Architecture Patterns Index]] #Decoupling #ApplicationArchitecture
# Command Pattern

This is a behavioural design pattern that turns a request into a stand alone object that contains all information about that request. You can then process the command at a convenient time, pass method arguments with it, queue it, and support rollback operations.

To illustrate the problem this pattern solves, imagine a UI button. You give the base class the basic functionality, then subclass it for all of the different implementations (Save, open, close, OK etc). The number of subclasses balloons and any change to the Parent Button class risks breaking something.

Then you also have the problem that some of that functionality, Saving for example, will need to be accessible from other places so you either have to copy it around, make the other places rely on the button, or extract it out into some kind of utility class.

This last option of a utility class is effectively what the command pattern does. It creates a Command object (the command being to Save in our example) and all places in the GUI that need to use Saving functionality invoke it. The request is then passed on to the back-end places that need to know.
![[Pasted image 20241129140111.png]]
All your commands should implement the same interface, usually a really simple one with just an Execute method. This means any request sender can use any Command, and you can even switch them at runtime. Any parameters that need sending should be bundled up with the command.

![[Pasted image 20241129140548.png]]

### References

[Command](https://refactoring.guru/design-patterns/command)