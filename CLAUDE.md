# sdc-videos

> Public GitHub Pages site (geljic.github.io/sdc-videos) for SDC explainer video drafts made with Reel, so DoE staff can watch and leave timestamped review notes from behind the DoE Zscaler filter (it blocks gigglebooth.online as "Unknown").

## Scope
- Files live in `projects/sdc-videos/`. Own git repo, origin github.com/Geljic/sdc-videos (PUBLIC), pushed as Geljic with the Geljic noreply email.

## Rules
- Everything here is public on the internet. Only videos Simon has said can be public. No internal data files, no scripts.
- One folder per video: `<slug>/index.html` (review page: DoE-styled copy of `projects/gelibeans/tools/review-page/index.html`
  with a Sections list) + `video.mp4` (re-encoded: `ffmpeg -c:v libx264 -preset slow -crf 24 -movflags +faststart -c:a aac -b:a 128k`,
  keep each file well under GitHub's 100 MB limit) + `poster.jpg`. Add a card to the root `index.html`.
- Sources and renders stay in Reel (`projects/reel/data/projects/<id>/`, script in `projects/reel/examples/`).
- Review notes come back from the reviewer as pasted Markdown; `projects/gelibeans/tools/review-page/note-frames.py` turns them into frames.
