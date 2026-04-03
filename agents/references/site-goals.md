# Site Goals

## Project

Personal academic website for Eric Quintane, built with MkDocs.

## Current Pages

- `Home`
- `About`
- `Research`
- `Teaching`

## Site Identity

The site should feel:

- modern
- sophisticated
- minimal
- academic
- credible
- clear

It should not feel:

- beige or warm-tinted
- decorative for its own sake
- generic faculty-template bland
- promotional or self-important
- visually inconsistent

## Current User Preferences

- white background
- modern type system
- fewer font switches
- disciplined scale across pages
- smaller homepage hero title
- efficient use of above-the-fold space
- clear hierarchy on the About page

## What Already Works

- navigation
- the idea of the At a Glance panel
- the presence of About, Featured Research, and Teaching/Public Work on the
  homepage
- the recent direction of the inner pages

## Core Constraints

- Keep the site simple.
- Do not add unnecessary pages.
- Preserve factual accuracy.
- Respect the professional identity of an academic scholar site.
- Design and content changes should support one another rather than compete.

## File Ownership Summary

- Design changes: `docs/stylesheets/extra.css`
- Content changes: markdown copy files in `docs/`
- Structure changes: `mkdocs.yml` plus markdown section order and wrappers

## Build Command

```bash
./.venv/bin/mkdocs build
```
