# Lexit Course Repository

This repository is public to enable branch protections on our plan. Do not push any sensitive or copyrighted material.

What is allowed

- Student-authored notes and summaries
- Lightweight metadata and links

Not allowed

- Proprietary PDFs or course handouts (keep them in private systems)
- Model solutions or answer keys (the `solutions/` folder is intentionally not part of this public repo)
- Credentials, tokens, or personal data

Branch workflow

- Weekly branches: `KW<week>-<year>` (e.g., `KW29-2025`)
- Each week is squash-merged into `main`
- Previous week is archived as `(Archive) KW<week>-<year>` for at least two weeks, then deleted automatically

Protections

- `main`: PRs only, linear history, no force-push, no deletions
- `KW*`: push allowed but no force-push; fast-forward only
- `(Archive) *`: read-only

Weekly protection pattern

If your weekly branches look like `KW31-2025`, `KW01-2024`, `KW52-2030`, you can cover them with one ruleset pattern:

- Pattern: `KW*-*`
- Why it works:
  - `KW` → fixed literal prefix
  - `*` → matches any number of characters (week number)
  - `-` → literal dash
  - `*` → matches any number of characters again (year)
Apply the same settings as above (no force-push, linear history). Our automation also applies per-branch protection if rulesets are not used.

License

- See LICENSE for terms. Consider Creative Commons BY-NC-SA 4.0 for student summaries.
