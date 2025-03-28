[[Architecture Patterns Index]] #SaaS #ApplicationArchitecture
# 12 Factor App

This is a methodology for building SaaS apps. It was originally developed by Heroku to help developers create robust, scalable, and maintainable applications.

The 12 factors:
- Codebase: one codebase, tracked in VCS, many deploys
- Dependencies: Explicitly declared and isolated
- Config: Stored in the environment
- Backend Services: treated as attached resources
- Build, Release, Run: strictly separate build and run stages
- Processes: execute the app as one or more stateless processes
- Port binding: export services via port binding
- Concurrency: scale out via the process model
- Disposability: maximise robustness with fast startup and graceful shutdown
- Dev/prod parity: keep development, staging and production as similar as possible
- Logs: treat as event streams
- Admin processes: Run admin/management tasks as one-off processes

![[Pasted image 20250314121225.png]]

**Advantages**
- Scalability - by promoting the use of stateless processes it becomes easier to scale
- Portability - dependencies are isolated so apps can easily be moved between different environments
- Continuous deployment - separate build, run and deploy stages aid this
- Configuration management - separating config from codebase aids portability and repeatability even more
- Resilience - the focus on disposability and transience helps this because failures etc can be handled gracefully

**Disadvantages**
- Complexity - especially if you use all 12 factors
- Learning curve is high
- Overhead can be introduced
- Can be detrimental if not necessary - smaller apps might not benefit from this methodology
### References

[The Twelve-Factor App (12factor.net)](https://12factor.net/)
[Twelve-Factor Methodology in a Spring Boot Microservice | Baeldung](https://www.baeldung.com/spring-boot-12-factor)