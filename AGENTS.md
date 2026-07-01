# Logos & Icons — Agent Guide

## Repository Purpose

Store SVG logos and icons of brands, technologies, and tools for use in GitHub README and portfolio website. Assets are sourced as clean SVGs (official brand assets, hand-optimized, or recreated from scratch) — never raster images, never embedded fonts.

## Directory Pattern — Strict

Every entity gets its own directory at the repository root named in lowercase-kebab-case:

```
<entity-name>/
  logo-light.svg     # dark/black fill → for light backgrounds
  logo-dark.svg      # light/white fill → for dark backgrounds
  logo-default.svg   # (optional) brand colors → for colored display
```

### Examples

```
react/
  logo-light.svg     # black React icon
  logo-dark.svg      # white React icon
  logo-default.svg   # blue React icon

pi/
  logo-light.svg     # black Pi logomark
  logo-dark.svg      # white Pi logomark
```

## File Rules — Required

- All SVGs must include `xmlns` and `viewBox` attributes.
- Prefer `viewBox="0 0 800 800"` for square icons, but preserve original proportions.
- Paths must be optimized — no editor metadata, invisible layers, embedded raster images, scripts, CSS, or XML comments beyond minimal structural notes.
- Indent with 2 spaces.
- `logo-light.svg` → fill color `#000` (black).
- `logo-dark.svg` → fill color `#fff` (white).
- `logo-default.svg` → original brand color(s).

## What Agents Must Never Do

- Never modify this AGENTS.md or .gitignore without explicit permission.
- Never add npm, Python, or build tooling — no package.json, no scripts, no config files beyond .gitignore and AGENTS.md.
- Never add WebP, PNG, JPG, or any raster format. SVGs only.
- Never embed fonts or use `<style>` or `<script>` tags.

## Adding a New Logo

1. Create a directory at root using lowercase-kebab-case (e.g., `visual-studio-code/`, not `vscode/` or `VS_Code/`).
2. Add at minimum `logo-light.svg` and `logo-dark.svg`. Add `logo-default.svg` when brand colors add value.
3. Update README.md — add the new entry to the asset table so the user knows it exists.
4. Commit with conventional commit message: `feat(entity): add <name> logo` or `feat(entity): add <name> logo assets`.

## Raw GitHub URLs

Since directories are flat at root level, every asset URL is predictable:

```
https://raw.githubusercontent.com/arijit/logos-and-icons/main/<entity>/logo-light.svg
https://raw.githubusercontent.com/arijit/logos-and-icons/main/<entity>/logo-dark.svg
https://raw.githubusercontent.com/arijit/logos-and-icons/main/<entity>/logo-default.svg
```
