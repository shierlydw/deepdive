# Shierly Dewi — Portfolio

Senior UX Designer portfolio. Static site, no build step, no dependencies.

## Contents

```
index.html              the whole site (home + 2 case studies), ~200 KB
assets/images/          img_1 … img_18  +  ds_img_1 … ds_img_19  (.jpg, .png where transparent)
assets/videos/          video_1 … video_4  +  ds_video_1, ds_video_2  (.mp4)
ASSETS.md               what each numbered file shows, grouped by section
UPLOAD.md               how to merge this into the existing repo safely
```

`index.html` contains three views: the home page, the Multigenerational
Family Banking case study, and the Scaling a Design System slide deck.
The case studies open as overlays — there are no other HTML pages.

## Running it locally

Open `index.html` in a browser. Videos may not autoplay from `file://`
in some browsers; if so, serve it instead:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Updating the existing repo

Upload `index.html` and `assets/` **together, in the same commit** — see
`UPLOAD.md` for which old files get overwritten and which can be deleted.

## Publishing on GitHub Pages

`index.html` must sit at the repository root. Either push the *contents*
of this `site/` folder to the root, or push `site/` as-is and set Pages
to deploy from that folder.

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main`, Folder: `/ (root)` or `/site`
4. Save. Live at `https://<username>.github.io/<repo>/` within a minute or two.

## Editing

- All CSS and JS are inline in `index.html`.
- To swap an image, replace the file in `assets/images/` keeping the same
  filename and extension. See `ASSETS.md` to find the right number.

## Fonts

Loaded from Google Fonts (Inter, Inter Tight, Geist, Onest). Requires an
internet connection; falls back to system sans-serif offline.
