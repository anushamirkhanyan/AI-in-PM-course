# AI in PM Course — Workspace

This repo is a hands-on workspace for the *AI in Project Management* course. It's
where course exercises turn into real, working Claude Code building blocks:
**skills**, **agents**, and small **projects**.

## Layout

```
.claude/
  agents/     Custom subagents — specialists Claude can delegate to
  skills/     Custom skills — reusable, packaged instructions (slash commands)
projects/     Standalone course projects/exercises, one folder each
CLAUDE.md     Persistent context Claude Code reads at the start of every session
```

## Getting started

- Open a session in this repo and Claude Code automatically reads `CLAUDE.md`
  for context — no need to re-explain the project each time.
- Try the example skill: type `/standup-notes` and paste in some rough notes.
- Try the example agent: ask Claude something like "use the risk-spotter agent
  to review this project plan" (see `.claude/agents/risk-spotter.md`).
- Start a new course project by adding a folder under `projects/`, e.g.
  `projects/01-status-report-generator/`.

## Adding your own skill or agent

- **Skill** — add `.claude/skills/<skill-name>/SKILL.md` with a short
  description (when it should trigger) and step-by-step instructions.
- **Agent** — add `.claude/agents/<agent-name>.md` with YAML frontmatter
  (`name`, `description`, optional `tools`) and a system prompt describing
  its role.

As the course progresses, each new concept (prompting, agents, MCP, workflows)
gets its own folder or file here so the whole thing builds into a working
portfolio.
