# 07-280 Field Guide

A study guide for CMU 07-280 (Intro to AI & ML), rebuilt from the course slides
and notes with intuition, full derivations, worked examples, interactive figures
and guided problems. Updated through the semester as new lectures come out.

## Run it

```sh
python3 -m http.server 4280
```

Then open http://localhost:4280. No build step, no dependencies — plain HTML,
with KaTeX loaded from a CDN for the math.

## Layout

| | |
| :-- | :-- |
| `index.html` | Home and chapter map |
| `*.html` | One page per chapter, plus `practice.html` and `cheatsheet.html` |
| `assets/site.js` | Shared shell: sidebar, prev/next, table of contents, quizzes, math. The `CHAPTERS` array at the top defines the site's structure. |
| `assets/style.css` | All styling and components |

## Adding a chapter

1. Copy an existing chapter as a starting point; set `<body data-page>` to the
   new filename without `.html`.
2. Add it to `CHAPTERS` in `assets/site.js`, and add a card to `index.html`.
3. Every `<h2>` needs an `id` — the table of contents is built from them.
4. Page scripts go inside `document.addEventListener("shellready", …)`.

Figures marked as reconstructions were rebuilt because the original PDF images
didn't survive text extraction — check them against the slides.
