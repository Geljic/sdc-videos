# Handover: sdc-videos

Updated 2026-11-19: first version added as its own page.

## Start here (paste as the first prompt of the next session)
> Continue sdc-videos (projects/sdc-videos). Read CLAUDE.md and HANDOVER.md first, then work down "Next" from 1.

## State
- Public repo Geljic/sdc-videos, GitHub Pages from main: https://geljic.github.io/sdc-videos/
- `rcr/`: "Better ways of working with the RCR Framework" draft v6 (Reel project `sdc-rcr`, voice DoE-Voice-Main `1c5fd70b` at speed 1, raw + Reel-finished clips with a 0.45 s hold, 2:29), review page for the SDC manager. v4 fixed his 3 notes (black edge on push/slide transitions, BA too early, broken handshake icon); v5 fixes cut-off narration (voice at 1.15 dropped line endings; checked end to end with Reel `scripts/vo-final-check.ts`).
- `rcr-v1/`: the very first render (Reel `renders/sdc-rcr-v1.mp4`, demo voice, 2:34), kept for comparison at Simon's ask: https://geljic.github.io/sdc-videos/rcr-v1/. publish.py puts the newest slug first in the list; reorder videos.json + index.html by hand if the current draft should stay on top.
- Publish with the skill: `python3 .claude/skills/video-review-page/publish.py VIDEO --slug rcr --version "draft vN" --dir projects/sdc-videos --owner Simon --section "m:ss Name" ...` (writes videos.json + root index, pushes, waits for Pages).

## Next (priority order)
1. **Manager's notes on draft v6** of `rcr/`: paste them → `python3 .claude/skills/video-review-page/note-frames.py notes.md VIDEO OUT/` → fix in Reel (`data/projects/sdc-rcr`) → voice/coverage checks → render → publish.py with the next version.
2. **Share the `video-review-page` skill with the SDC team** (Simon's ask): zip it or add it to this repo under `skill/`; Simon hadn't picked which.

## Gotchas
- Publish with `.claude/skills/video-review-page/publish.py` (pushes as Geljic with the noreply email); it rewrites the root index.html from videos.json.
- DoE Zscaler blocks advice.gigglebooth.online ("Miscellaneous or Unknown"); github.io gets through.
- Reviewer notes live in his browser's localStorage only, keyed by the video path: keep the file name `video.mp4`.

## Key files
- `CLAUDE.md`: rules. `index.html`: list of videos. `<slug>/index.html` + `video.mp4` + `poster.jpg`.

## History
- 2026-11-19: first version published as `rcr-v1/`.
- 2026-11-18: project created; RCR video v3 published; v4 after the manager's notes, published with the video-review-page skill.

## 2026-11-24: RCR draft v7 (built on ZimaOS, PC offline)
- Clinton's notes: graphic SFX removed (Demucs vocals stem only, no_vocals dropped), 0:36 and 0:57 lines re-voiced with VoiceStudio DoE-Voice-Main, shots frozen to fit; 2:32.
- New lofi bed from music-craft `sdc-rcr-bed-v7` (original bed is on the PC).
- Sections timestamps shifted in rcr/index.html. The Reel project `data/projects/sdc-rcr` on the PC is now behind v7; v7 was patched from the v6 render, not re-rendered in Reel.
