# Claude Repository

## Overview

This repository (`ideonfilho-stack/Claude`) is a document storage repository, not a software project. It currently holds archived web content for reference purposes.

## Repository Contents

| File | Type | Description |
|------|------|-------------|
| `IMC v12 — Fertilizantes (Cloud).webarchive` | Apple Safari Webarchive | Saved web page: IMC v12 – Fertilizantes cloud tool (922 KB) |

The `.webarchive` format is a macOS/Safari-specific format that bundles HTML, images, scripts, and other web resources into a single binary file. It cannot be opened on non-Apple platforms without conversion tools.

## Branch Structure

| Branch | Purpose |
|--------|---------|
| `main` | Primary branch |
| `claude/claude-md-docs-*` | AI-assisted documentation branches (auto-created) |

## Working with This Repository

### Adding New Archive Files

When uploading webarchive or other document files:

```bash
git add "filename.webarchive"
git commit -m "Add <description> webarchive"
git push -u origin main
```

### Viewing a Webarchive on macOS

Double-click the `.webarchive` file in Finder — Safari opens it directly.

### Converting Webarchive on Linux/Windows

```bash
# Extract resources with python-webarchive or similar tools
pip install webarchive
python -c "import webarchive; webarchive.open('file.webarchive').extract('output/')"
```

## Conventions

- File names follow the pattern: `<Tool/Document Name> v<version> — <Category> (<Environment>).webarchive`
- No code lives in this repository; no build, test, or lint steps exist.
- Commit messages should be descriptive about the content being archived (e.g., `Add IMC v12 fertilizer cloud tool archive`).

## Notes for AI Assistants

- There is no application code to build, test, or lint.
- Do not run package managers (`npm`, `pip`, `cargo`) — no dependency manifests exist.
- File additions and README updates are the primary operations in this repository.
- The primary language of the stored content appears to be Portuguese (Brazil).
