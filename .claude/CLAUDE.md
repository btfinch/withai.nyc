# CLAUDE.md - withai.nyc Public Website

## Purpose

This is the **public website repo** for WithAI Research, Inc. It hosts legal documents and the company landing page at `withai.nyc`.

**IMPORTANT:** This repo is PUBLIC. Do not add any proprietary code, secrets, or internal business documents here.

## Relationship to Other Repos

| Repo | Visibility | Purpose |
|------|------------|---------|
| `withai.nyc` (this repo) | PUBLIC | Legal pages, landing page |
| `withai-extension` | PRIVATE | VS Code extension source code |

The extension links to pages hosted here (`withai.nyc/terms`, `withai.nyc/privacy`).

## Hosting

- **Platform:** GitHub Pages
- **Domain:** `withai.nyc` (custom domain via CNAME)
- **Deploy:** Push to `main` branch, GitHub Pages auto-deploys

## Files

```
withai.nyc/
├── .claude/
│   └── CLAUDE.md      # This file
├── index.html          # Landing page
├── terms.html          # Terms of Service
├── privacy.html        # Privacy Policy
├── CNAME               # Custom domain config for GitHub Pages
└── README.md           # Setup instructions and context
```

## Updating Legal Docs

1. Edit `terms.html` or `privacy.html`
2. Update the "Last updated" date in the file
3. Commit and push to main
4. Changes go live in ~1 minute

## Contact

- Legal contact: ben@withai.nyc
- Company: WithAI Research, Inc.
