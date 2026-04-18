# assets

This repository is a shared, version-controlled store for static assets used across multiple websites/projects.

## 1) Purpose

Use this repo to host reusable static files so projects can reference one source of truth instead of duplicating files.

Current live domain (GitHub Pages / CNAME): `assets.lukihackwell.com`.

## 2) Current vs target structure

### Current compatibility structure (kept to avoid breakage)

- `css/` and `stylesheet/` are both currently allowed.
- `bootstrap/` is currently treated as legacy vendor-style storage.

### Target structure (incremental, non-breaking)

```text
assets/
├── brand/
│   ├── logos/
│   ├── favicons/
│   ├── social-preview/
│   └── colors/
├── css/
│   ├── core/
│   ├── components/
│   ├── pages/
│   └── vendor/
├── js/
│   ├── core/
│   ├── components/
│   └── vendor/
├── images/
│   ├── backgrounds/
│   ├── illustrations/
│   ├── screenshots/
│   └── thumbnails/
├── icons/
│   ├── svg/
│   ├── png/
│   └── favicon/
├── fonts/
├── manifests/
├── vendor/
├── websites/
│   ├── theinfo/
│   ├── networkluki/
│   ├── ipconfig/
│   └── lukihackwell/
├── docs/
├── bootstrap/      # legacy path, do not remove yet
├── stylesheet/     # legacy path, do not remove yet
├── index.html
└── README.md
```

## 3) Naming conventions (governance baseline)

- lowercase only
- hyphens only (`site-header.css`, not `Site_Header.css`)
- descriptive names (`home-hero-background.webp`)
- no spaces

## 4) Allowed file formats

- Icons/logos: prefer `.svg`
- Web images: prefer `.webp`/`.avif`
- Transparent raster: `.png` when needed
- Photos: `.jpg` only when suitable
- Styles/scripts: `.css`, `.js`
- Fonts: `.woff2` preferred
- App metadata: `.webmanifest`, `.json`

## 5) Optimization rules

- Compress images before commit.
- Prefer modern formats (`.webp`, `.avif`, `.svg`) for web delivery.
- Avoid oversized assets; CI warns/fails on very large files.

## 6) Reuse policy across projects

- Prefer shared/common assets in top-level category folders.
- Use `websites/<site-name>/` only when an asset is truly site-specific.
- Do not copy the same binary into multiple folders; deduplicate and reuse.

## 7) Deprecation and versioning policy

- Do not rename/remove active files without migration notice.
- For breaking updates, publish new versioned paths (example: `vendor/lib/v2/`).
- Keep legacy paths (`bootstrap/`, `stylesheet/`) until consumers migrate.

## 8) Security and operational rules

- Do not commit secrets or keys.
- Treat SVG as untrusted input; disallow embedded scripts/event handlers.
- Vendor assets must include source/version/license notes in PR description.
- Keep filenames stable and cache-friendly; use versioned filenames/paths for breaking changes.

## 9) Key docs

- `docs/ASSET_RULES.md` — detailed governance and safety rules.
- `CONTRIBUTING.md` — contribution checklist and review expectations.
- `asset-manifest.json` — optional machine-readable asset index.
