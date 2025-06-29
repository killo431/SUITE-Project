
# Agent & Project Orchestration Strategy

## AI Agent Roles
- Planner: breaks goals into tasks
- Architect: defines infrastructure
- DevAgent: generates modular code
- DocGen: writes structured documentation
- OpsAgent: handles deployments and workflows

## Context Loading via ai-config.json
- Injects goals, architecture, team roles, specs
- Shared across AutoGen, CrewAI, and LangGraph

## Orchestration Flow
1. Project created via `/create-project.sh`
2. `ai-config.json` generated from templates
3. Agents loaded with context from `/agents/context`
4. Prompts selected based on phase from `/library/prompts/`
5. Output delivered to `/home/builder/project/` folders

## Reset System
- Manual or automated reset clears `/projects`, `/var`, AI memory, logs
- Snapshots saved in `/projects/<name>/snapshot/`
- Rules, prompts, and vocab preserved across sessions

## Smart Enhancements (Optional)
- Multi-model routing
- Snapshot + rollback automation
- Cloud sync & remote task server (via REST or N8N)
