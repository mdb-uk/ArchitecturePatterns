
[[Architecture Patterns Index]]
# Adapter Pattern

The Adapter pattern is a structural design pattern that allows objects with incompatible interfaces to communicate.

Often you will have two components or systems that use different languages to communicate (such as XML and JSON for example). This means that you would need to make changes to one system (or both) so that they can communicate. However with the Adapter pattern there is another alternative.

The problem:
![[Pasted image 20241029150043.png]]

The solution:
![[Pasted image 20241029150055.png]]

When using the Adapter pattern you create a new object (or microservice etc) that sits between the two systems. It accepts communication in one or both of the formats, and is capable of outputting in the opposite format. I.e. JSON to XML. Thus the two systems can communicate via the Adapter.

![[Pasted image 20241029150417.png]]

Some disadvantages of this approach is that the complexity increases and the Adapter becomes a single point of failure.