# Efficient Studio — QC Standard (MVP Baseline)

## Purpose
Prevent silent quality decay and ensure every output is reviewable and reproducible.

## QC gates
### Gate A — Fragment QC (≤30s rule)
Each fragment (max 30 seconds) must pass before batch merge.

Pass criteria (minimum):
- Visual: no obvious artifacts, flicker, broken anatomy, unstable frames
- Audio: no clipping, clear speech, no missing segments
- Subtitles (if present): readable, synced, no broken encoding
- Content: matches script intent, no random hallucinated elements
- Language: correct target language (no mixing unless intended)

Fail actions:
- Fix and re-render the fragment
- Log the failure reason in Operator Notes

### Gate B — Final Combined Review
After merging all fragments:
- continuity (audio/visual)
- pacing
- subtitle consistency
- branding consistency (if used)
- final export settings correct

## Operator Notes (required on Fail)
Minimal template:
- Fragment ID / time range
- Fail reason category (visual/audio/subtitle/content/language)
- Action taken (rerender/edit/replace)
- Outcome (pass/fail)

## Pass/Fail Matrix
Create and maintain:
- docs/30_qc/pass-fail-matrix.md  (next step)

## Storage rules
- QC notes live in repo (text)
- Big media artifacts go to docs/90_artifacts or external storage, never in root

## MVP next steps
1) Add pass-fail-matrix.md
2) Add a simple “QC checklist” for operators
3) Link QC gates into Sacred JSON (qc_gates section)