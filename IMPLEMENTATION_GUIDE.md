# 🚀 DeTechIT Universal Project Suite – IMPLEMENTATION GUIDE

This guide outlines the complete structure, logic, and execution framework of the DeTechIT Project Suite (DUPS) using Linear and multi-agent orchestration.

---

## I. 🧱 Core System Architecture

Permanent folders:
- `/bin`: Common CLI tools (e.g. python, node, npm)
- `/lib`: AI/system libraries
- `/etc`: Configuration files (envs, keys)
- `/var`: Logs and runtime data
- `/opt`: LLMs, embeddings, weights
- `/home/builder/project`: Runtime sandbox per project

---

## II. 📂 Project Structure Per Instance

Subdirectories inside `/home/builder/project/`:
- `src/`: Application source code
- `config/`: Runtime configs
- `data/`: Development/test datasets
- `models/`: Small fine-tuned or shared models
- `logs/`: App or agent logs
- `tests/`: Unit/integration/E2E tests
- `docs/`: Markdown-based project documentation

---

## III. 📚 Documentation Requirements

- `README.md`: System-level overview
- `MANIFEST.md`: Index of files and purposes
- `goals.md`: Measurable business/tech goals
- `architecture.md`: System structure and interactions
- `specs_overview.md`: Functional + non-functional specs
- `metrics.md`: KPIs to track
- `decisions.md`: Project decisions log
- `roadmap.md`: Phase tracking
- `reset_log.md`: Reset history
- `snapshot_guides.md`: How to export/restore state

---

## IV. 🧠 Prompt + Rule Intelligence

Prompt structure:
- `/library/prompts/base/`: Global prompts
- `/library/prompts/dynamic/`: Context-derived
- `/library/prompts/project-goal-maps/`: Goal-to-prompt mappings

Rule structure:
- `/library/rules/`: JSON/YAML constraint and safety rules

Validation process:
- Use `PromptImprovementChecklist.md` to ensure every prompt is high-quality before use.

---

## V. 🤖 AI Agent Roles

Agents and their responsibilities:
- `Planner`: Converts goals to backlogs
- `Architect`: Designs systems
- `DevAgent`: Modular, testable code
- `DocGen`: Documentation & changelogs
- `OpsAgent`: CI/CD, deployment automation
- `Data Analyst`: KPIs, validation
- `AI Interviewer`: Stakeholder feedback

Configuration:
- `ai-config.json`, `agents.json`, `/agents/context/`, `vocab.json`

---

## VI. 🔧 Linear Integration

Workspace configuration:
- **Projects**: 1 per live project folder
- **Milestones**: Core, Design, Validation, Deploy
- **Labels**: phase:*, ai-agent:*, output:*
- **Views**: filtered by agent, phase, file type

Issue Templates:
- 4 task templates (one per major phase) are prewritten
- Linked files included in descriptions
- Prompts tagged and routed based on goal/phase

---

## VII. 🔁 Reset & Snapshot System

Reset:
- Clears `/projects`, logs, memory
- Logs to `reset_log.md`

Snapshots:
- Saved in `/snapshot/`
- Mapped in `snapshot-index.md`

---

## VIII. 📦 Deployment & Export Options

- `.zip` files for each versioned release
- Compatible with Claude, Cursor, Linear, and GitHub
- Optional: Notion, Git template, or prompt server

---

## IX. 🔄 Future-Ready

Planned features:
- Prompt versioning system
- Prompt REST API
- Claude/OpenAI routing fallback
- Plugin system
- Live performance dashboard

---

This guide is structured for AI parsing, team use, and scalable project orchestration.
