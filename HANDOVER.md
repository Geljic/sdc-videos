# Handover: sdc-videos

Updated 2026-11-18 after project set up.

## Start here (paste as the first prompt of the next session)
> Continue sdc-videos (projects/sdc-videos). Read CLAUDE.md and HANDOVER.md first, then work down "Next" from 1.

## State
- Public repo Geljic/sdc-videos, GitHub Pages from main: https://geljic.github.io/sdc-videos/
- `rcr/`: "Better ways of working with the RCR Framework" draft v5 (Reel project `sdc-rcr`, voice DoE-Voice-Main `1c5fd70b` at speed 1, 2:13), review page for the SDC manager. v4 fixed his 3 notes (black edge on push/slide transitions, BA too early, broken handshake icon); v5 fixes cut-off narration (voice at 1.15 dropped line endings; checked end to end with Reel `scripts/vo-final-check.ts`).
- Publish with the skill: `python3 .claude/skills/video-review-page/publish.py VIDEO --slug rcr --version "draft vN" --dir projects/sdc-videos --owner Simon --section "m:ss Name" ...` (writes videos.json + root index, pushes, waits for Pages).

## Next (priority order)
1. Act on the manager's review notes for `rcr/` (paste → note-frames.py → fix in Reel → re-render → replace video.mp4, bump "draft vN").

## Gotchas
- DoE Zscaler blocks advice.gigglebooth.online ("Miscellaneous or Unknown"); github.io gets through.
- Reviewer notes live in his browser's localStorage only, keyed by the video path: keep the file name `video.mp4`.

## Key files
- `CLAUDE.md`: rules. `index.html`: list of videos. `<slug>/index.html` + `video.mp4` + `poster.jpg`.

## History
- 2026-11-18: project created; RCR video v3 published; v4 after the manager's notes, published with the video-review-page skill.
