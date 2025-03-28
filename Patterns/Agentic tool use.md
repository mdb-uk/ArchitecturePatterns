[[Architecture Patterns Index]] #AI #Agent
# Agentic tool use

By using tools, Agents are no longer limited to their training data and can reach out to other sources such as the internet.

- Input 
- Reasoning
- Tool selection and use
- Synthesis and processing
- Output

The LLM can dynamically select tools to use as it is operating based on the processing needs. 

Components of this pattern involve:

- Tool invocation - The agent identifies a tool that it needs to use to achieve it's task and generates a function call to invoke it
- Function schema - Tools are defined using a schema that describes their names, descriptions and parameters
- Execution - The Agent executes the tool's function and processes the result when it is returned from the external tool, integrating these results into it's workflow

Three primary tool types:
- Extensions
- Functions
- Data Stores

#### Extensions

Extensions allow Agents to interact with APIs regardless of their implementation. Like the [[Adapter Pattern]] in a sense.

The traditional coding approach would be to take some parameters and arrange them in the correct way to call the API and then handle the response. But if the caller leaves out some parameters for example this will not work properly. This is where extensions can come in. 

An extension teaches the Agent how to use an API with examples, and teaches it what parameters are successfully needed to call the given endpoint. Then it can use it's Model to interact with the caller/user to get any missing data required to successfully call the API.

![[Pasted image 20250328102604.png]]

"To summarize, Extensions provide a way for agents to perceive, interact, and influence the outside world in a myriad of ways. The selection and invocation of these Extensions is guided by the use of Examples, all of which are defined as part of the Extension configuration."

#### Functions

- Similar to Extensions, but do not make live api calls
- Functions are executed on the Client-side, extensions are executed on the agent-side
![[Pasted image 20250328102645.png]]

- Logic of calling the API is offloaded back to the client-side application
- This may be desirable for many reasons including the fact the API calls might need to be made by another custom application (or layer of the application), or security/auth restrictions that prevent the Agent doing it, timing considerations etc
- Also additional data transformation logic requirements on the API response might mean you want to use functions over extensions

![[Pasted image 20250328102702.png]]
### Data stores
(p27)

By default an LLM only has access to the data it was trained on. Data stores are like an extension to this that able the Agent to have access to other information, that can be updated.

![[Pasted image 20250328102726.png]]

For Gen AI Agents, Data Stores are typically implemented as a Vector Database that the dev wants the Agent to have access to at runtime. They store data in the form of vector embeddings, a type of high-dimensional vector or mathematical representation of the data provided. The RAG pattern uses Data Stores. 

![[Pasted image 20250328102746.png]]
1. User query is sent to the embeddings model to generate the embeddings for the query
2. The embeddings are matched against the contents of the vector database using a matching algorithm like SCaNN
3. The matched content is retrieved from the vector database in text format and set back to the agent
4. The Agent receives the user query and the retrieved content and can respond via it's model
5. Final response is sent to user

Example that includes RAG with ReAct reasoning/planning: 

![[Pasted image 20250328102806.png]]


### References

[AI Agents: Mastering the Tool Use Design Pattern - Part 4 | Microsoft Community Hub](https://techcommunity.microsoft.com/blog/educatordeveloperblog/ai-agents-mastering-the-tool-use-design-pattern---part-4/4393804)

[Agentic Design Patterns Part 3: Tool Use](https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-3-tool-use/)