# ericquintane.github.io

Personal website for Eric Quintane, built with MkDocs and published on GitHub Pages.

## Project Structure

- `docs/`: MkDocs source content, including the homepage, portrait, and custom styles
- `mkdocs.yml`: MkDocs configuration
- `.github/workflows/deploy.yml`: GitHub Actions workflow for MkDocs-based Pages deployment

## Local Development

Create or reuse the local virtual environment, then run:

```bash
./.venv/bin/mkdocs serve
```

To build the site locally:

```bash
./.venv/bin/mkdocs build
```

## Publishing Notes

The site is published through GitHub Pages using the workflow in `.github/workflows/deploy.yml`.
The source content lives in `docs/`, and the generated output is deployed by GitHub Actions.

## GitHub Pages Settings

The repository is configured for GitHub Pages deployment via Actions:

1. In `Settings -> Pages`, keep `Source` set to `GitHub Actions`.
2. Keep the custom domain set to `www.quintane.net`.
3. Future content changes should only require editing the MkDocs source files and pushing to `main`.
