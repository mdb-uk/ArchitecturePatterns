[[Architecture Patterns Index]]
# Composite design pattern

This is a **Structural** design pattern that lets you compose objects into tree structures and then work with these structures as if they were individual objects.

This pattern only makes sense when the core object model of your application can be represented using a tree structure. For example:

![[Pasted image 20241105155058.png]]

Determining the total price of a complex order using traditional methods could be tricky - you cannot just loop through all the items in the order because they are all different classes and you wouldn't know in advance what might be in there. You would have to infer the classes dynamically which gets messy.

The composite pattern helps with this problem by defining a common interface which in the above example exposes a method for calculating the price of the item. If the item was a parent of sub items it would include all their prices (i.e. passing the request down the tree). You could then easily tally up these costs for all sub items to get the total. The big benefit of this approach is you do not need to know or care about the concrete classes of the objects that make up the 'tree', they can all be treated the same via the interface they all implement.

![[Pasted image 20241105155732.png]]