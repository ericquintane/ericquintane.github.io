# Coordinator

## Purpose

Coordinate the website improvement process across three maker agents and three
reviewer agents without letting them overwrite one another or drift away from
the site's goals.

## Read First

1. `agents/references/site-goals.md`
2. `agents/references/design-charter.md`
3. `agents/references/acceptance-checklist.md`
4. `agents/references/design-rubric.md`
5. `agents/references/content-rubric.md`
6. `agents/references/structure-rubric.md`

## Team Topology

- `design-maker.md` + `design-reviewer.md`
- `content-maker.md` + `content-reviewer.md`
- `structure-maker.md` + `structure-reviewer.md`

## Recommended Order

1. Structure maker
2. Structure reviewer
3. Coordinator integrates accepted structure changes
4. Content maker
5. Content reviewer
6. Coordinator integrates accepted content changes
7. Design maker
8. Design reviewer
9. Coordinator integrates accepted design changes
10. Local build and final human review

Run the pairs in this order unless there is a strong reason not to. For this
site, overlapping edits create more confusion than speed.

## Ownership Rules

- Structure maker owns `mkdocs.yml` and structural changes in markdown files.
- Content maker owns the prose in `docs/index.md`, `docs/about.md`,
  `docs/teaching.md`, and `docs/research.md`.
- Design maker owns `docs/stylesheets/extra.css` and only tiny markup changes
  needed to support styling.
- Reviewer agents are read-only.
- If two makers need the same file, the coordinator decides sequencing rather
  than letting them edit in parallel.

## Coordinator Responsibilities

- Write a short task brief for the current round.
- Pass only the relevant files and rubric to each agent.
- Reject edits outside an agent's scope.
- Compare reviewer feedback against maker intent.
- Integrate only the useful changes.
- Run `./.venv/bin/mkdocs build` after each integrated round.
- Keep a running list of unresolved questions for the human.

## Prompt Template For Makers

Use a short prompt shaped like this:

```text
Goal:
Files you may edit:
Files you must not edit:
Primary rubric:
Current concern:
Deliverable:
```

## Prompt Template For Reviewers

Use a short prompt shaped like this:

```text
Scope:
Files reviewed:
Rubric:
Task:
Return findings only, ordered by severity, then a short recommendation.
```

## Acceptance Standard

Only accept a change if it satisfies the acceptance checklist and improves the
site on at least one important dimension without noticeably damaging another.

The human is the final decision maker. No change is accepted until the human
has previewed it and said to keep it.

## Output Format For Integrated Rounds

Keep a simple running log:

```text
Round:
Agent:
Accepted:
Rejected:
Why:
Follow-up:
```

## When To Convert This Into Skills

Do not convert these briefs into skills immediately. Use them for two or three
real site-improvement rounds first. If the workflow proves stable, then create
skills from the briefs and rubrics with the same scopes.
