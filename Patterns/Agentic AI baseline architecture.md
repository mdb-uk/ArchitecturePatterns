[[Architecture Patterns Index]]
# Agentic AI baseline architecture

"This article provides a baseline architecture for building and deploying Agentic AI Systems that use frameworks like AutoGen, LangChain, LlamaIndex or Semantic Kernel."

[Baseline Agentic AI Systems Architecture | Microsoft Community Hub](https://techcommunity.microsoft.com/blog/machinelearningblog/baseline-agentic-ai-systems-architecture/4207137)

Agentic AI systems are designed to resolve complex problems with little human interaction/supervision. 

These systems are comprised of multiple agents that can converse with each other. They can be organised centrally or self-organised in a decentralised manner.

The agents can perform **planning**, can be augmented with **memory** and use **tools**.

Because agents can take actions there are risks associated with these systems therefore proper architecture and sandboxing is essential. 

![[AgenticAISystems_ACA.png]]

Key components:

- Azure AI Studio
	- Prompt flow 
	- Managed online endpoints
	- Azure AI dependencies:
		- Azure Storage Account
		- Azure AI Search
		- Azure KeyVault
		- Azure Container Registry
		- Azure OpenAI Service
		- Azure AI Services
			- Document Intelligence
			- Azure Speech
			- Content AI Safety
- Azure Cosmos DB
- Azure Cache for Redis
- Azure API Management
- Azure Container Apps
- Azure Service Bus
- Azure Kubernetes Services (optional)

Alternative architecture using AKS:
![[AgenticAISystems_AKS.png]]