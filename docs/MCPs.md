
# Modular Control Plane (MCP) Overview

## Purpose
Enable distributed agent orchestration, code generation, data transformation, and workflow automation.

## Recommended MCP Platforms

### 1. AutoGen (OpenAI)
- Role-based agent orchestration
- Multi-model prompt routing
- Ideal for: coding agents, doc generation

### 2. LangGraph
- Graph-based state-machine for agents
- Memory, multi-hop chains, dynamic context
- Ideal for: persistent workflows and retrievers

### 3. CrewAI
- Simple team-of-agents model
- Built-in memory and tool usage
- Ideal for: planning, interviewing, advisory agents

### 4. N8N
- Visual low-code workflow builder
- Integrated with APIs, databases, code runners
- Ideal for: event-based triggers, deployment pipelines

### 5. LangChain + SuperAgent
- Advanced LLM + toolchain orchestration
- Modular agent tools and fallback handling

## Integration Strategy
- Deploy all MCPs via Docker Compose or cloud functions
- Use shared context folder and `/library/` for common access
- Route tasks via project-defined AI config file (`ai-config.json`)
