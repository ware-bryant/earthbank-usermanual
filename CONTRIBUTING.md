# Contributing to the EarthBank User Guide

This documentation is plain Markdown, one task-focused page per file, organised into numbered folders under `docs/`. There's no build step to run locally beyond `mkdocs serve` if you want a preview — GitHub Pages handles the rest on merge.

## Making a change

1. Fork this repo (or create a branch, if you have write access).
2. Edit the relevant `.md` file. If your change doesn't fit an existing page, add a new file to the appropriate numbered folder and add it to the `nav:` list in `mkdocs.yml` so it shows up in the site navigation.
3. Open a pull request describing what changed and why. Screenshot updates are welcome and encouraged — drop new images in `docs/assets/images/` and reference them with a relative path, e.g. `![Map window toolbar](../assets/images/map-toolbar.png)`.
4. A maintainer reviews and merges. The site rebuilds automatically.

## Style notes

- Use "EarthBank" (not "AusGeochem" or "AuScope EarthBank" mid-sentence — "AuScope EarthBank" is fine on first mention/headings, "EarthBank" thereafter).
- Prefer short, task-titled pages over one long page — this mirrors how `io.lithosurfer.userdoc` is organised for the API docs.
- Name UI elements in the text itself (e.g. "click **Add Sample**"), not only via a screenshot — screen readers and search can't see images, and screenshots go stale faster than button labels do.
- Keep screenshots current. If you notice one that no longer matches the live platform, either fix it in the same PR or open an issue.
- Don't commit personal data, credentials, or unpublished/private sample data in screenshots.
