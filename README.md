# AstroJoeBretz.github.io

Landing page for <https://astrojoebretz.github.io/>. Plain HTML and CSS: no build step, no JavaScript, no frameworks, no external requests.

It introduces Joe Bretz and links to research visual stories, publications, code, and profiles. Each story lives in its own repo and is served at `/<repo>/` on the same domain. This repo only links to them.

## Layout

| Path | Purpose |
|---|---|
| `index.html` | The page |
| `css/style.css` | All styles (light theme; tokens at the top) |
| `assets/` | Thumbnails, profile photo, `og-image.png` (1200x630) |
| `404.html` | Not-found page |
| `.nojekyll` | Stops GitHub running Jekyll |

## Add a story card

1. Put the thumbnail (2:1, under 150 KB) in `assets/thumbnails/`.
2. In `index.html`, copy the `<article class="card story">` block inside `#stories`, then change the link, image, kicker, title, blurb, meta line and button URLs.
3. Link to the story with a root-relative URL and trailing slash, e.g. `/my-new-story/`.
4. Commit and push.

Each story's footer should link back to this page ("All stories").

## Deploy

1. Create a **public** repo named exactly `AstroJoeBretz.github.io`.
2. Push these files to `main`.
3. Settings, Pages, Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Open <https://astrojoebretz.github.io/> after about a minute.

Story links return 404 until the story repo (`cosmic-singing-bowls`) is deployed from its own Pages workflow.

The `handoff/` folder and `prof_photo.png` (the full-size original) are listed in `.gitignore` and are not published.
