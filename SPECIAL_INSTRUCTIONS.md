# 📌 Special Instructions for Implementing DeTechIT Projects

This document defines strict implementation rules and boundaries for any AI agent or developer working within the DeTechIT Universal Project Suite (DUPS).

---

## 1. 📁 Stick to File Structure

- All **code** must go into `/home/builder/project/src/`
- All **configs** into `/config/`
- All **documentation** into `/docs/`
- All **tests** into `/tests/`
- All **logs or runtime** files must go to `/logs/`
- Never place production files in root directories

---

## 2. ✅ Use Only Defined Prompts and Goals

- All implementation must trace back to `goals.md` or `specs_overview.md`
- Every prompt must follow `PromptImprovementChecklist.md` before use
- Use `/library/prompts/` or generate clean prompts tagged by phase/goal

---

## 3. 📓 Document Every Step

- Log reasoning and decisions in `decisions.md`
- Update `architecture.md` when new modules are added or changed
- Maintain traceability between AI prompt → file → Linear task

---

## 4. 🚫 No Scope Drift

- Only build what’s described in `goals.md`, `Linear`, or the current Claude task
- Do not invent features, endpoints, UI pages, or abstractions without being explicitly asked
- When in doubt, pause and request clarification

---

## 5. 🧾 Naming Conventions

- Files: `kebab-case` (e.g., `user-auth.module.ts`)
- Variables: `camelCase`
- Classes/Components: `PascalCase`
- Prefix all shared functions or endpoints with module name (e.g., `authLoginUser`)

---

## 6. 🤖 Respect AI Role Responsibilities

- DevAgent: Code and unit test only
- DocGen: Write/format docs, Markdown, and changelogs
- Planner: Translate goals to tasks
- Architect: Maintain system design and boundaries

> Use `ai-config.json` to check your role. Never cross boundaries unless assigned.

---

## 7. 📤 Output Format Rules

- Clearly label every output with:
  ```
// File: /src/auth/login.ts
```
- Use inline comments for clarity in all files
- Never generate ZIPs, scaffolders, or full template blobs
- Return Markdown when writing docs, and code-only when writing implementation

---

If assumptions must be made, **log them in `decisions.md`** immediately and default to minimal, secure design.
