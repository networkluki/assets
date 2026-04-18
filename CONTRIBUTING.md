# Contributing

## Pull request checklist

- Put files in the correct folder.
- Follow naming rules (lowercase + hyphens only).
- Optimize image assets before commit.
- Avoid adding duplicate binaries.
- Verify links in `README.md` and `index.html`.
- For vendor assets, include source/version/license in PR notes.

## Validation

This repository includes a GitHub Actions workflow for lightweight checks:

- invalid filenames
- oversized assets
- duplicate assets
- basic SVG safety patterns
- broken local links in docs/index
