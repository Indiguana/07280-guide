# 07-280 Field Guide

Static study-guide site for CMU 07-280. Plain HTML, no build. Serve with
`python3 -m http.server 4280`.

When adding or revising a chapter from new lecture material, use the
`teaching-site` skill (it lives in the gamechanger repo at
`.claude/skills/teaching-site/`). The conventions it describes are the ones this
site was built with:

- Pages write only `<main>`; `assets/site.js` injects the shell. Register every
  page in its `CHAPTERS` array.
- `<body data-page>` equals the filename; every `<h2>` has an `id`.
- Verify every number in `python3` before writing it.
- Never write a caption describing results that no code produced.
- Mark reconstructed figures as reconstructions.

Before finishing, run the skill's validator over this directory:

```sh
python3 <path-to-gamechanger>/.claude/skills/teaching-site/scripts/check_pages.py .
```
