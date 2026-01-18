# Sacred JSON Change Rules (Audit Gate)

This folder contains the project “source of truth” JSON.
It must stay stable, reviewable, and versioned.

## Hard rules
1) Any change to Sacred JSON requires:
   - a Decision Log entry: docs/40_decisions/Decision_Log_v1_0.md
   - a short review note in the commit message: WHY + WHAT changed
2) No direct edits without Decision Log entry.
3) One intent per commit (atomic changes).
4) Sacred JSON must never contain secrets or personal data.

## Versioning
- File name is stable: sacred_master.json
- Update the "version" field inside JSON on every approved change.

## Allowed content
- Architecture modules & boundaries
- Data flow / orchestration rules
- QC gates & pass/fail criteria pointers
- Roadmap pointers (not the full roadmap text)

## Not allowed
- Passwords, tokens, API keys, private emails,s, phone numbers
- Large dumps of docs, logs, exports
- “Temporary experiments” (put those into docs/00_inbox or docs/90_artifacts)