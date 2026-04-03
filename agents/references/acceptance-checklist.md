# Acceptance Checklist

Every future agent round should be judged against this checklist before any
change is accepted.

## Universal Checks

- Does the proposal solve the specific problem named in the brief?
- Is it better than the approved baseline, not just different?
- Did the agent stay within its scope?
- Did the proposal avoid creating new problems elsewhere?
- Does `./.venv/bin/mkdocs build` pass?

## Design Checks

- White background preserved
- One font family preserved
- No extra decorative effects introduced
- No increase in typography inconsistency
- Homepage hero uses space efficiently
- No dead whitespace introduced by the hero's side content
- Portrait or profile image does not awkwardly crop the subject
- About page reads more consistently, not less

## Content Checks

- More specific without becoming narrower than intended
- Less generic without sounding promotional
- No invented or uncertain facts
- No increase in repetition across pages

## Structure Checks

- Clearer hierarchy at first glance
- No extra complexity
- Navigation unchanged unless explicitly approved
- Above-the-fold experience improved or preserved

## Decision Output

For every proposal, the coordinator should record:

```text
Problem tested:
Accepted changes:
Rejected changes:
Reason:
Better / same / worse than baseline:
Human approved:
```

If the answer is not clearly `better`, reject the change by default.
