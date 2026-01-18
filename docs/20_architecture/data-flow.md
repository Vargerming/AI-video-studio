# Data Flow (MVP)

## Inputs
- Brief / topic
- Script (master)
- Target languages list

## Pipeline
1) Script -> (optional) translation -> localized scripts
2) Asset generation
   - visuals (image/video)
   - voice/audio
   - subtitles/captions
3) Segment assembly (≤30s fragments)
4) QC Gate A: fragment QC (pass-fail matrix)
5) Batch merge
6) QC Gate B: final combined review
7) Publish package (final video + captions + metadata)
8) Analytics tracking (views/retention + QC outcomes)

## State tracking (minimal)
- status: planned -> generating -> qc_fragment -> merged -> qc_final -> published
- logs: operator notes + decision log refs (when rules change)