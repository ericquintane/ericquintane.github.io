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

## Switching To GitHub Actions

The repository is ready for GitHub Pages deployment via Actions, but the source still needs to be changed in GitHub:

1. Open `Settings -> Pages` in the GitHub repository.
2. Under `Build and deployment`, set `Source` to `GitHub Actions`.
3. Keep the custom domain set to `www.quintane.net`.
4. After the first successful Actions deployment, the committed root build artifacts can be removed and the workflow can become the single deployment path.
