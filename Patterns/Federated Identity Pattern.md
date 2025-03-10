[[Architecture Patterns Index]] 
# Federated Identity Pattern

This pattern delegates authentication to an external Identity Provider (IDP). This allows users to use a single identity across various applications.

### Key features
- Separation of Auth and application code
- Claims-based access control - the IDP issues tokens with 'claims' for the user, such as identity and roles. Apps use these claims to authorise access to features and resources
- SSO - users can access multiple apps without the need to sign in separately for each one. This is particularly useful in enterprise environments and for SaaS.
- Improved security and user management - by centralising auth, federated identity reduces the risk of security vulnerabilities and simplifies user management. User identities can be revoked centrally when needed

### Common use cases
- Enterprise SSO
- B2B apps
- SaaS apps

### Considerations
- Single point of failure - the IDP becomes a critical component so ensuring availability and reliability is critical
- RBAC - implementing this can give more granular access to resources
- Home realm discovery - determining which IDP to use for auth can be automated based on user input or other factors

![[Pasted image 20241119134421.png]]

### References

[Federated Identity pattern - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/patterns/federated-identity)