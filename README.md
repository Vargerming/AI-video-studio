# AI-video-studio

Documentation hub for an AI video production studio project.

## What this repo is (for now)
- Documentation only (no code while laptop/Ubuntu is offline)
- Clear structure to reduce chaos
- Source-of-truth documents will be added gradually after review

## Current priorities (next 2 weeks)
1) Define MVP roadmap (small, testable, repeatable)
2) Lock “Sacred JSON” audit gate (changes only via review)
3) Set QC baseline (30s fragment rule + final review)
4) Keep Decision Log append-only

## Repo structure
- docs/00_inbox/ — raw notes to be processed
- docs/10_roadmap/ — MVP roadmap & milestones
- docs/20_architecture/ — architecture & modules
- docs/30_qc/ — QC rules, pass/fail, operator notes
- docs/40_decisions/ — append-only decision log
- docs/50_sacred/ — sacred JSON gate & rules
- templates/ — templates for extraction and logging

## Rules
- No “dump everything” commits.
- Any core architecture or sacred JSON change requires review note in Decision Log.
