# Pass/Fail Matrix (MVP)

## How to use
- Apply to every fragment (≤30s) and to the final combined render.
- If any **FAIL** occurs → fix + re-render + add operator note.

| Area | Check | PASS | FAIL | Notes template |
|---|---|---|---|---|
| Visual | No flicker / frame jumps | stable | flicker/jumps | fragment_id, timestamp, symptom |
| Visual | No obvious artifacts | clean | artifacts/glitches | what/where |
| Visual | Anatomy/objects ok (if relevant) | plausible | broken/warped | what object |
| Audio | Speech clarity | clear | muffled/robotic | sample timestamp |
| Audio | No clipping | clean | clipping/distortion | peak moments |
| Audio | No missing segments | complete | cutouts | time range |
| Subtitles | Readable | readable | too small/garbled | screenshot ok |
| Subtitles | Sync | synced | desync | lead/lag secs |
| Language | Correct language | correct | mixed/wrong | expected vs got |
| Content | Matches script intent | aligned | drift/hallucination | mismatch |
| Export | Correct format/settings | ok | wrong codec/resolution | required specs |

## Operator Note (minimum)
- Fragment ID:
- Timecode:
- FAIL category:
- Fix action:
- Result: