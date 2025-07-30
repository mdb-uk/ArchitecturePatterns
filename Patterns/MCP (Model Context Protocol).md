[[Architecture Patterns Index]] #AI 

# MCP (Model Context Protocol)

MCP is a way for LLMs to more easily integrate with external tools.

On their own, LLMs can't integrate with other tools or your data sources. 

![Client -> MCP servers/adapters -> 3rd party APIs](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6de5b04a-5e6c-47cf-a81e-e332dd3570df_2906x990.png)

The MCP Server is essentially an Adapter ([[Adapter Pattern]]) between the LLM and the external tools.

MCP Servers for various external tools can be brought in like a software library to give your LLMs the ability to integrate with those external tools.

They are essentially wrappers around an external API that are able to communicate with the LLM. They implement standardised communication methods (such as STDIO and SSE)

Custom MCP servers can also be built though and simply need to accept the request from the LLM in the correct format, translate that request into the correct format for whatever external tool you wish to communicate with, and then send the request. Finally, the response received would be parsed back to the LLM format and returned to the LLM.

![[Pasted image 20250714142127.png]]
![[Pasted image 20250714142138.png]]
![[Pasted image 20250714142153.png]]

- An Agent can really just be thought of as a Microservice
- The MCP Host agent pulls in the MCP client library to create a client instance
- There will also be an MCP server (either yours or someone elses)
- The server has capabilities to offer, things like tools, resources, prompts - all bound by the MCP specs in the way it is offered
- stdio can be used to communicate between the MCP host and MCP server in a local environment
- More enterprise situations will use HTTP/SSE to communicate, and messages will be in JSON/RPC formats
- MCP servers can send async messages back to the client as well
- The client agent can interrogate the resources of servers it knows about
- The client will use it's LLM model to process the NL input and work out what capabilities it might need to achieve the ask
- In the definition of the tools/capabilities you include the way it works, params etc, so the LLM can decide how that needs to be invoked and therefore your actual agent doesn't need to be programmed to know how to do any of that
- The model recommends a course of action  and the Agent's client code makes the decision and actually invokes the capabilities (potentially with HITL input)
- MCP clients/servers are composable - a server can be a client itself to achieve other aims
![[Pasted image 20250730140103.png]]
### References

[MCP (Model Context Protocol): Simply explained in 5 minutes](https://read.highgrowthengineer.com/p/mcps-simply-explained)

[Model Context Protocol (MCP): Integrating Azure OpenAI for Enhanced Tool Integration and Prompting | Microsoft Community Hub](https://techcommunity.microsoft.com/blog/azure-ai-services-blog/model-context-protocol-mcp-integrating-azure-openai-for-enhanced-tool-integratio/4393788)

[Core architecture - Model Context Protocol](https://modelcontextprotocol.io/docs/concepts/architecture)

https://www.youtube.com/watch?v=FLpS7OfD5-s&list=WL&index=21