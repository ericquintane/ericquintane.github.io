# ericquintane.github.io

Personal website for Eric Quintane, built with MkDocs and published on GitHub Pages.

## Project Structure

- `docs/`: MkDocs source content, including the homepage, portrait, and custom styles
- `mkdocs.yml`: MkDocs configuration
- `.github/workflows/deploy.yml`: GitHub Actions workflow for MkDocs-based Pages deployment
- `index.html`, `css/`, `js/`, `assets/`, `search/`, `stylesheets/`, `webfonts/`: generated static site files currently committed at the repository root for branch-based GitHub Pages compatibility

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

At the moment, the live site is being served from the repository root by GitHub Pages. Because of that, after rebuilding with MkDocs, the generated contents of `site/` also need to be copied to the repository root so the published site stays in sync.

This was done with:

```bash
rsync -a site/ ./
```

If GitHub Pages is later switched in repository settings to deploy from `GitHub Actions`, the committed root build artifacts can be removed and the workflow can become the single deployment path.
