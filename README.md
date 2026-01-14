# withai.nyc - Public Website & Legal Documents

**Created:** January 14, 2026

## Overview

This repository hosts the public website for WithAI Research, Inc. at `withai.nyc`. It contains:

- **Landing page** (`index.html`) - Simple company page
- **Terms of Service** (`terms.html`) - Legal terms for WithAI VS Code extension
- **Privacy Policy** (`privacy.html`) - Privacy policy for WithAI VS Code extension

These pages are linked from the WithAI VS Code extension (welcome popup, settings panel).

---

## Context: What This Is For

WithAI Research is shipping a VS Code extension that provides:
- WYSIWYG markdown editor
- Claude Code settings management
- Workspace setup tools

The extension collects optional email/company info via a welcome popup (sent to Google Forms). Legal requirements necessitate Terms of Service and Privacy Policy documents. This repo hosts those documents.

**Why a separate repo?**
- The extension repo (`withai-extension`) is PRIVATE and contains proprietary code
- Legal pages need to be publicly accessible
- GitHub Pages requires a public repo (or paid GitHub Pro)
- Clean separation of concerns

---

## Setup Status

### Completed
- [x] Terms of Service drafted (adapted from Basecamp's open-source policies, CC BY 4.0)
- [x] Privacy Policy drafted
- [x] HTML pages created with clean styling
- [x] CNAME file configured for `withai.nyc`
- [x] Landing page created

### Next Steps

#### 1. Initialize Git Repo
```bash
cd /Users/btsfinch/ben-home/intersection-home/withai.nyc
git init
git add .
git commit -m "Initial commit: legal pages and landing"
```

#### 2. Create GitHub Repo
```bash
# Option A: Using GitHub CLI
gh repo create withai-research/withai.nyc --public --source=. --remote=origin --push

# Option B: Create via GitHub web UI, then:
git remote add origin git@github.com:withai-research/withai.nyc.git
git push -u origin main
```

**Note:** Replace `withai-research` with your actual GitHub org/username if different.

#### 3. Enable GitHub Pages
1. Go to repo Settings → Pages
2. Source: Deploy from branch
3. Branch: `main`, folder: `/ (root)`
4. Save

#### 4. Configure DNS (at your domain registrar)

Add these A records for apex domain:
```
Type    Host    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
```

Or for www subdomain:
```
Type    Host    Value
CNAME   www     withai-research.github.io
```

#### 5. Enable HTTPS
After DNS propagates (can take up to 48 hours, usually faster):
1. Go to repo Settings → Pages
2. Check "Enforce HTTPS"

#### 6. Verify
```bash
curl -I https://withai.nyc/terms
curl -I https://withai.nyc/privacy
```

---

## Updating Documents

To update legal docs:

```bash
cd /Users/btsfinch/ben-home/intersection-home/withai.nyc

# Edit the file (e.g., terms.html)
# Update the "Last updated" date in the file

git add .
git commit -m "Update terms: [description of change]"
git push
```

Changes deploy automatically in ~1 minute.

---

## File Structure

```
withai.nyc/
├── .claude/
│   └── CLAUDE.md       # Instructions for Claude Code
├── index.html          # Landing page (withai.nyc)
├── terms.html          # Terms of Service (withai.nyc/terms)
├── privacy.html        # Privacy Policy (withai.nyc/privacy)
├── CNAME               # Custom domain configuration
└── README.md           # This file
```

---

## Legal Attribution

Terms and Privacy Policy adapted from [Basecamp's open-source policies](https://github.com/basecamp/policies), used under CC BY 4.0 license. Attribution included in page footers.

---

## Contact

- Email: ben@withai.nyc
- Company: WithAI Research, Inc.
