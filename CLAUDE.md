# AI in PM Course — Project Context

## What this repo is

A learning workspace for a Project Management professional taking the
"AI in PM" course. It exists to build practical, working Claude Code
artifacts — not just notes — as each course concept is covered:

- **Skills** (`.claude/skills/`) for repeatable PM workflows (status reports,
  meeting prep, risk logs, retros, etc.)
- **Agents** (`.claude/agents/`) — specialist subagents for PM-flavored tasks
  (risk spotting, research, summarizing, drafting)
- **Projects** (`projects/`) — self-contained exercises/deliverables from the
  course, one subfolder per project

## Working style

- The user is a PM, not a software engineer — prefer plain language,
  explain *why* before diving into implementation details, and avoid
  unnecessary engineering jargon.
- Keep new skills and agents small and focused on one PM task each rather
  than broad, do-everything tools.
- When starting a new course project, create it under `projects/<NN-name>/`
  with its own short README describing the exercise's goal.
- Favor Markdown/HTML deliverables (status reports, plans, dashboards) that
  are easy to read and share — offer to publish them as Artifacts when that
  fits the request.

## Conventions

- Skill files: `.claude/skills/<skill-name>/SKILL.md`
- Agent files: `.claude/agents/<agent-name>.md`
- Course projects: `projects/<NN-short-name>/`
