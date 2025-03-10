 [[Architecture Patterns Index]]
# Strangler

The Strangler pattern, also known as the Strangler fig pattern, incrementally migrates a legacy system to a new system.

It works thusly:

1. Facade creation - the facade is created to intercept requests to the legacy system and route them either to the new system or the legacy system
2. Incremental replacement - specific pieces of functionality are gradually replaced with new applications and services behind the facade
3. Seamless transition - Users continue to interact with the system unaware of the transition happening gradually behind the scenes
4. Complete migration - eventually the old system is "strangled" i.e. all functionality is moved over to the new system and the old one can be decomissioned.

Benefts

- Reduces risk by breaking the migration down into smaller pieces that are more manageable to migrate
- Continuous operation: the legacy system remains operational during the migration, ensuring no disruption to users (and providing a rollback if needed)
- Flexibility: new features can be added at any pace

Challenges

- Complex routing - if there are a lot of services in play then routing and network configs can become complex
- Rollback plans - each migration step requires a plan in case of issues

![[Pasted image 20240806114849.png]]

![[Pasted image 20240806114919.png]]


References

[The pros and cons of the Strangler architecture pattern | Enable Architect (redhat.com)](https://www.redhat.com/architect/pros-and-cons-strangler-architecture-pattern)

[Strangler Fig pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/strangler-fig)