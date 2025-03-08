# Links

[[Architecture]] [[Architecture Patterns Master Index]]
# Content

https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch01.html

The most common architecture pattern, also known as the n-tier architecture.

Components are organized into horizontal layers, each performing a specific role within the application such as presentation or business logic.

There is not a specified number or type of layers in the pattern, however most layered pattern systems consist of four standard layers:

- presentation
- business
- persistence
- database

Note that sometimes this pattern is referred to as the Four Layer Architecture, and in that case you would only find the exact 4 layers described above.

Sometimes the business and persistence layers can be combined together in smaller applications, and larger applications might well have more layers.

The layers are abstractions around how to achieve their specific tasks and know nothing about the workings of the other layers besides the interfaces between layers (separation of concerns).

![[Pasted image 20240223154343.png]]

The Closed indicator means that each layer can only communicate with the one next to it - for example the presentation layer would have no knowledge of or references to the persistence layer. This is known as layers of isolation and means that changes in one layer will only potentially affect the layer directly above it.

There are times when Open layers can be used. For example, if the business layer has some shared components you might consider making these into a layer of their own, i.e. Services layer, which would sit beneath the Business Layer and therefore be accessed by it only. However this then means the Business Layer has to go through the Services layer in order to reach the Closed Persistence layer, which does not make sense.
![[Pasted image 20240223155244.png]]
In the above example, the Services layer is made open so that the Presentation layer still cannot contact it, but the Business layer has the ability to bypass it to get to the Persistence layer.

It is a solid general purpose pattern and often a good starting point. It's easy to develop and very testable. There are a couple of things to watch out for:

- Architecture sinkhole antipattern: requests flow through unnecessary pass-through layers where little or no logic is performed. All layered architecture systems will have some requests like this, but the percentage is key. If the ratio is reversed you might consider making some layers open or another pattern
- This pattern does tend towards monolithic applications even if you separate your layers into individual deployable units
- Deployment can be tricky (often having to redeploy entire app) and it's not very agile
- Not very scalable
- Not very performant