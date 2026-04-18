# assets

This repository is a **central place for static files** (assets) that can be reused across multiple websites/projects.

## What is this used for?

Use this repo to store and version:

- images (`images/`)
- icons (`icons/`)
- CSS (`css/` and/or `stylesheet/`)
- JavaScript (`js/`)
- Bootstrap-related files (`bootstrap/`)

The goal is a clear structure so the same files can be referenced from multiple pages without duplication.

## Recommended folder structure

```text
assets/
├── bootstrap/      # Bootstrap css/js or custom bootstrap extensions
├── css/            # Custom stylesheets
├── icons/          # SVG/ICO/PNG icons
├── images/         # JPG/PNG/WebP/GIF etc.
├── js/             # Custom JavaScript files
├── stylesheet/     # Existing/legacy css structure (can be kept)
├── index.html      # Simple information page
└── README.md       # Documentation
```

## Example usage from another page

```html
<link rel="stylesheet" href="https://<your-domain>/assets/css/main.css" />
<script src="https://<your-domain>/assets/js/main.js" defer></script>
<img src="https://<your-domain>/assets/images/logo.png" alt="Logo" />
```

## Naming and organization

- Use lowercase letters and hyphens in filenames, e.g. `site-header.css`.
- Avoid spaces and special characters in filenames.
- Keep shared/common files here; keep project-specific files inside each project.

## Quick checklist before commit

- Is the file in the correct folder?
- Is the filename clear and consistent?
- Do affected pages reference the correct path?
