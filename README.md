# Our Journey — Story Timeline

A single-page, scroll-driven visual timeline of Medical Outreach PJ's outreach programmes. Pure static site — no build step, no dependencies.

## What's in here

- `index.html` — the whole site (structure, styling, and behaviour)
- `timeline.json` — the data: every moment (date, location, programme, ordered photos, captions, collage groupings)
- `logo.png` — header logo
- `Video/` — all 240 photos/videos, organized by programme → location → date, matching the paths referenced in `timeline.json`

## How it works

- Scroll down and each moment fades/zooms into view as it enters the viewport.
- A thin progress rail on the left fills as you scroll through the whole page.
- Photo groups with 4+ items auto-scroll sideways on desktop (pause on hover); on touch devices they become a natural swipeable strip instead — continuous auto-motion is disorienting and battery-heavy on phones, so touch gets swipe-to-browse instead.
- Tap/click any photo to open it full-size, with prev/next and (for the two paired photos in Padawan Kuching) a stacked collage tile.
- Two moments have no confirmed date yet (Partner NGO/B40 "post covid", Supplies/Supply COVID) — they sit in a "Needs a date" section at the bottom.

## Editing content later

Everything renders from `timeline.json` — add a caption by filling in the `"caption"` field for an image, or group two photos into a collage tile by giving them the same `"collageGroup"` value. No HTML editing required for data changes.

## Deploying to GitHub Pages

1. Create a new repo and push this folder's contents to it (as the repo root, or into a `docs/` folder — either works).
2. In the repo: **Settings → Pages → Build and deployment → Source** = "Deploy from a branch", pick the branch and the folder you pushed to (`/ (root)` or `/docs`).
3. Save. GitHub gives you a URL like `https://<username>.github.io/<repo-name>/` within a minute or two.

That's it — no build process, so there's nothing else to configure.
