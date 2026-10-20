# Contributing to the EarthBank User Guide

This documentation is plain Markdown, one task-focused page per file, organised into numbered folders under `docs/`. There's no build step to run locally beyond `mkdocs serve` if you want a preview — GitHub Pages handles the rest on merge.

## Making a change

1. Fork this repo (or create a branch, if you have write access).
2. Edit the relevant `.md` file. If your change doesn't fit an existing page, add a new file to the appropriate numbered folder and add it to the `nav:` list in `mkdocs.yml` so it shows up in the site navigation.
3. Open a pull request describing what changed and why. The manual is currently text-only — please don't add screenshots for now (they go stale quickly as the platform develops). If one is ever genuinely needed, discuss it in an issue first.
4. A maintainer reviews and merges. The site rebuilds automatically.

## Style notes

- Use "EarthBank" (not "AusGeochem" or "AuScope EarthBank" mid-sentence — "AuScope EarthBank" is fine on first mention/headings, "EarthBank" thereafter).
- Prefer short, task-titled pages over one long page — this mirrors how `io.lithosurfer.userdoc` is organised for the API docs.
- Name UI elements in bold in the text (e.g. "click **Add Sample**") and describe where they are on screen, so readers can follow along without images.
- Don't include personal data, credentials, or unpublished/private sample data in examples.
