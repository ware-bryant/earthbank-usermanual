# EarthBank User Documentation

Source for the AuScope EarthBank platform **user manual**, built with [MkDocs](https://www.mkdocs.org/) and the [Material theme](https://squidfunk.github.io/mkdocs-material/), published to GitHub Pages.

This is the end-user counterpart to [`io.lithosurfer.userdoc`](https://github.com/lithodat-pty-ltd/io.lithosurfer.userdoc), which covers the EarthBank API for developers. This repo covers using the platform itself: registering, finding and viewing data, contributing data, visualising data, and citing the platform. The API section here is intentionally short — it links out to `io.lithosurfer.userdoc` rather than duplicating it.

## Status

All text content from the source "AusGeochem User Guide 2.0_Sep24_Review Copy.docx" has been migrated: rebranded (AusGeochem → EarthBank; "AuScope Geochemistry Network (AGN)" retained), reorganised into the task-based structure below, and lightly rewritten so UI elements are named in the text.

**No screenshots, by design (for now).** The manual is text-only: every UI element is named in bold in the text (e.g. **Add Sample**), which keeps pages accessible and searchable and avoids images going stale as the platform develops. Screenshots may be added later if needed.

**What's not done yet:**

- **Currency check.** Content hasn't been verified against the live platform, so some described workflows may have changed. Flag anything that's drifted as you find it.
- **Front-page introduction.** `docs/index.md` has a placeholder intro — a proper one is coming once the team has a new introduction paragraph ready.
- **Data window "Meta Data" section** was an unfinished placeholder in the source manual (`docs/01_finding-and-viewing-data/data-window.md`) — needs real content from the team.
- **How to Cite** — worth confirming whether a citation for "AuScope EarthBank" (as opposed to the original "AusGeochem" papers) exists or is planned.

## Local preview

```bash
pip install mkdocs-material
mkdocs serve
```

Then open http://127.0.0.1:8000/.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Short version: fork or branch, edit the relevant `.md` file under `docs/`, open a pull request describing the change. Every page has an "Edit this page" link (bottom of the page on the published site) that jumps straight to the GitHub editor for that file.

## Deployment

`.github/workflows/deploy.yml` builds and publishes `docs/` to GitHub Pages automatically on every push to `main`. No manual build step required.

## Setting this up on GitHub

1. Create a new repo (personal account is fine to start) and push this folder to it.
2. In the repo's **Settings → Pages**, set the source to **GitHub Actions** (the included workflow handles the build).
3. Update `mkdocs.yml`'s `site_url`, `repo_url`, and `repo_name` to match wherever the repo actually lives (see the note at the top of that file).

### Moving to a project/org account later

Yes — this is a normal, well-supported GitHub operation, and nothing about this repo makes it harder:

- **Full transfer** (Settings → General → Danger Zone → Transfer ownership, on the repo): moves the repo, its full git history, issues, and PRs to the new account/org in place. Anyone who has it cloned just needs to update their remote URL. The only thing that changes automatically is the GitHub Pages URL (it now includes the new account/org name), so update `site_url`/`repo_url` in `mkdocs.yml` afterwards and re-run the Pages deploy.
- **Fresh push**, if a full transfer isn't wanted (e.g. you'd rather keep the personal repo around too): add the new org repo as a second git remote and push `main` to it. Slightly more manual, keeps both copies independent.

Either way, no content needs to change — just the three config lines above and the Pages source setting.
