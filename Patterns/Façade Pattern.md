14:56 | 2024-10-29
# Links

[[Software design patterns Master Index]]
# Content

This structural pattern involves a class or component sat in front of another and providing a simplified interface to the other component.

This can avoid coupling client systems to the complicated system - they are instead loosely coupled to the façade which could easily be swapped out.

![[Pasted image 20241029150651.png]]

Disadvantages include the face the façade can become a ['god object']([God object - Wikipedia](https://en.wikipedia.org/wiki/God_object)) coupled to all classes of an app.