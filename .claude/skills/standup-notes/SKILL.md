---
name: standup-notes
description: Turn rough bullet notes or a stream-of-consciousness update into a clean, structured standup/status update (Did / Doing / Blockers). Use when the user pastes raw notes and wants a polished update to share with a team or stakeholders.
---

# Standup Notes

Convert messy notes into a short, structured status update.

## Steps

1. Read the raw notes the user provides (pasted text, or a file if they name one).
2. Organize the content into three sections:
   - **Did** — what was completed since the last update
   - **Doing** — what's in progress now
   - **Blockers** — anything stuck, at risk, or needing a decision/help
3. Keep each bullet short (one line), specific, and in plain language —
   no filler, no restating the obvious.
4. If something in the notes doesn't clearly fit Did/Doing/Blockers, ask the
   user rather than guessing where it goes.
5. Output the result as plain Markdown the user can paste directly into
   Slack, email, or a status doc.
