[[Architecture Patterns Index]] #AI 

# MCP (Model Context Protocol)

MCP is a way for LLMs to more easily integrate with external tools.

On their own, LLMs can't integrate with other tools or your data sources. 

![Client -> MCP servers/adapters -> 3rd party APIs](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6de5b04a-5e6c-47cf-a81e-e332dd3570df_2906x990.png)

The MCP Server is essentially an Adapter ([[Adapter Pattern]]) between the LLM and the external tools.

MCP Servers for various external tools can be brought in like a software library to give your LLMs the ability to integrate with those external tools.

They are essentially wrappers around an external API that are able to communicate with the LLM. They implement standardised communication methods (such as STDIO and SSE)

Custom MCP servers can also be built though and simply need to accept the request from the LLM in the correct format, translate that request into the correct format for whatever external tool you wish to communicate with, and then send the request. Finally, the response received would be parsed back to the LLM format and returned to the LLM.

### References

[MCP (Model Context Protocol): Simply explained in 5 minutes](https://read.highgrowthengineer.com/p/mcps-simply-explained)

[Model Context Protocol (MCP): Integrating Azure OpenAI for Enhanced Tool Integration and Prompting | Microsoft Community Hub](https://techcommunity.microsoft.com/blog/azure-ai-services-blog/model-context-protocol-mcp-integrating-azure-openai-for-enhanced-tool-integratio/4393788)