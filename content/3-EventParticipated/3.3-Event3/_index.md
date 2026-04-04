---
title: "Event 3"
date: 2026-03-21
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Summary Report: "FCAJ Community Day"

### Event Objectives

- Introduce GoTymeX and career opportunities in the technology field
- Share insights about DevOps in the era of Generative AI (GenAIOps)
- Provide knowledge on how modern AI systems are built and operated
- Help attendees better understand DevOps pipelines and AI systems

### Speakers

- **Hai Bui** - Engineering Manager, GoTymeX
- **Phuc Dang** - Cloud Architect, GoTymeX
- **Phap Nguyen** - Cloud Engineer, VPBank
- **Phat Pham** - Software Engineer, Katalon
- **Nghi Danh** - AI Engineer, Renova Cloud
- **Phong Nguyen** - Senior Software Engineer, Sympli
- **Thinh Nguyen** - DevOps Engineer, FCAJ

### 1. Introduction to GoTymeX

GoTymeX is an organization or group operating in technology and digital finance. It is described as being among the Top 100 globally influential corporations, with a focus on building modern technology systems for the fintech industry.

Main areas:

- Digital banking
- Financial technology (fintech)
- Large-scale technology systems

The event also mentioned that GoTymeX is hiring, especially for roles related to software engineering, DevOps, and AI.

### 2. GenAIOps Essential – DevOps for Generative AI Applications

#### Why has DevOps become essential?

Systems are increasingly:

- Complex
- Distributed

They require:

- Automation
- Continuous delivery
- Fast scalability

#### Traditional DevOps on AWS

Flow:

- Code
- Build
- Test
- Release
- Deploy
- Operate
- Monitor

Toolchain:

- Planning: Git, Jira
- CI: Jenkins
- Build: Maven, Gradle
- Test: JUnit
- Deploy: Docker
- Monitor: logging tools

#### CI/CD on AWS

Pipeline:

- Developer
- GitHub
- AWS CodePipeline
- AWS CodeBuild
- Amazon ECR
- Amazon ECS

Characteristics:

- Multi-stage pipeline for dev and prod
- Includes a manual approval step
- Infrastructure managed with CloudFormation as IaC

#### Key DevOps Capabilities

- Continuous Integration (CI)
- Continuous Delivery / Deployment (CD)
- Infrastructure as Code (IaC)
- Monitoring & Logging
- Collaboration

#### GenAIOps Pipeline

Flow:

- Define use case
- Model selection
- Model adaptation
- Prompt engineering
- RAG
- Fine-tuning
- App integration
- Deployment
- Monitoring

#### Monitoring for AI

Track:

- User input
- Model output
- Latency

The feedback loop helps:

- Improve the model
- Debug hallucinations

#### AgentCore (AI runtime)

An agent includes:

- Instruction
- Tools
- Context
- Memory

Runs on:

- Amazon Bedrock

#### Main insight

- DevOps is evolving into GenAIOps
- AI systems need pipelines similar to software systems

### 3. Shipping Code in the Agentic Era

#### Agents writing code in a new workflow

Flow:

- Assign tasks to agents such as Claude, Codex, or Kiro
- The agent creates a branch
- Code, commit, and push
- Create a pull request and merge

#### Multi-agent system

- One agent handles one task

It can:

- Spawn multiple sub-agents
- Run in parallel

#### Pi-messenger architecture

Input:

- User goal
- Task list

Core:

- Spawn sub-agents
- Manage lifecycle

Output:

- Completed tasks
- Validated code

Capabilities:

- Parallel execution
- Event-driven behavior
- Dependency-aware processing

#### Current limitations

- Can handle only one repository at a time
- No long-term memory
- Still requires human supervision

Conclusion:

- Coding agents are not yet fully production-ready

Future improvements:

- Multi-repo orchestration
- Custom toolchains
- Remote management

#### Main insight

- AI will not replace developers
- AI will become a teammate that supports developers

### 4. Production-Grade Multimodal GenAI on AWS

#### AI is a system, not only a model

The AI application stack includes:

- Agent & Orchestration
- RAG system
- Vector store
- Embeddings
- Infrastructure
- Hardware

#### Foundation Models vs Traditional ML

Traditional ML:

- Trained separately for each task
- Hard to scale

Foundation Models:

- Large pretrained models
- Support multiple tasks
- Q&A
- Translation
- Code generation

#### Multimodal AI

Input:

- Text
- Image
- Video
- Audio

All of these are embedded into vector space.

#### Nova Embeddings

- Dimensions range from 256 to 3072

Trade-off:

- Higher dimensions improve accuracy
- Lower dimensions improve speed

#### GraphRAG (advanced RAG)

Flow:

- Data such as PDF and CSV goes to Amazon S3
- Chunking and embedding
- Graph construction
- Indexing with vectors and graphs
- Query

Stack:

- Amazon Bedrock
- Amazon Neptune
- Amazon OpenSearch

Benefits:

- More accurate context
- Reduced hallucination
- Good scalability

#### Multi-agent workflow

Flow:

- User query
- Retrieve documents
- Evaluate relevance
- Search more if needed
- Generate answer

#### Agent architecture

- Prompt templates
- Planning and reasoning
- Tool calling
- Memory

Framework:

- LangGraph with nodes, edges, and state

#### Safety & Guardrails

Risks:

- Harmful content
- Prompt injection
- Data leakage

Solution:

- Amazon Bedrock Guardrails

### Event Experience

The event provided a clearer view of how DevOps can be combined with AI to build and operate modern systems. In particular, the GenAIOps and agent-based system topics highlighted how AI is managed in real-world environments.

Because some topics were highly advanced, much of the content was absorbed at a general level and would require further study for deeper understanding.

### Lessons Learned

- DevOps is evolving into GenAIOps in the AI era
- AI systems need complete pipelines just like software systems
- Agent-based architecture is an important trend
- AI will support developers rather than fully replace them

### Some Event Photos

![Event photo 1](/images/events/event3.jpg)

![Event photo 2](/images/events/event3_2.jpg)
