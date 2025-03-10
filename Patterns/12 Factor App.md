11:54 | 2024-09-30
# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

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

### References

[The Twelve-Factor App (12factor.net)](https://12factor.net/)
[Twelve-Factor Methodology in a Spring Boot Microservice | Baeldung](https://www.baeldung.com/spring-boot-12-factor)