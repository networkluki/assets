# Asset Rules

## Scope

These rules apply to all files in this repository.

## Naming

- lowercase letters only
- hyphens only
- descriptive filenames
- no spaces

## Format policy

- Prefer SVG for icons/logos.
- Prefer AVIF/WebP for web images.
- Use PNG only when transparency is needed.
- Use JPG for photos when modern formats are not practical.
- Prefer WOFF2 for fonts.

## Security checks

- SVG must not contain `<script>` tags.
- SVG must not include inline JS handlers like `onload=` or `onerror=`.
- Avoid `javascript:` URLs in any asset file.

## Vendor policy

- Third-party code should go in `vendor/` or `css/vendor/` or `js/vendor/`.
- Include source, version, and license in PR description.
- Update vendor assets regularly.

## Deprecation

- Never remove/rename in-use files without migration communication.
- Prefer additive versioning for breaking changes.
