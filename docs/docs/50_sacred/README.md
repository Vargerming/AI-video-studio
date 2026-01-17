# Sacred JSON Gate

The “Sacred JSON” is the master source-of-truth for the studio architecture.

## Rules
- Changes only via review/audit gate.
- Every change must be logged in docs/40_decisions/Decision_Log_v1_0.md
- Versioning required (e.g., v3.0.0 → v3.0.1)
- If unresolved contradictions exist, mark them as [UNRESOLVED] and do not patch silently.

## Status
- Sacred JSON exists outside this repo right now.
- Goal during hospital period: define the gate + decision log discipline.
- After laptop returns: import the Sacred JSON as a single file under docs/50_sacred/