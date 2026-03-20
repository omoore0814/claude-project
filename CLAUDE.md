# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

## Repository Overview

**Name:** claude-project
**Purpose:** Repository for Claude integration and projects
**Status:** Newly initialized — no source code has been added yet.
**Intended Stack:** Node.js / JavaScript (inferred from `.gitignore` template)

## Repository Structure

```
claude-project/
├── .gitignore       # Node.js/.JS comprehensive ignore rules
├── README.md        # Minimal project description
└── CLAUDE.md        # This file
```

## Current State

This repository contains only scaffold files. It is ready to receive a Node.js/JavaScript project. No framework, build system, test runner, or CI/CD pipeline has been configured yet.

## Development Conventions

### Branching

- Feature branches follow the pattern: `claude/<description>-<session-id>`
- Never push directly to `main` or `master` without explicit approval
- Always push with: `git push -u origin <branch-name>`

### Commits

- Use clear, descriptive commit messages that explain the "why"
- Commit messages should be concise (1–2 sentences)
- Sign commits using the configured SSH signing key

### Environment Variables

- Never commit `.env` files — they are gitignored
- Use `.env.example` to document required environment variables (this file IS committed)

### Ignored Paths (from `.gitignore`)

The `.gitignore` covers:
- `node_modules/`, `jspm_packages/`, `web_modules/` — dependency directories
- `dist/`, `out/`, `.next/`, `.nuxt/` — build output
- `coverage/`, `.nyc_output/` — test coverage reports
- `.cache/`, `.parcel-cache/` — bundler caches
- `*.log`, `*.pid` — runtime artifacts
- `.env`, `.env.*` (except `.env.example`) — secrets
- Framework-specific caches: `.svelte-kit/`, `.vitepress/`, `.docusaurus`, `.firebase/`

## Setting Up a New Project

When source code is added, update this file to include:

1. **Install dependencies** — e.g., `npm install` or `yarn install`
2. **Run the dev server** — e.g., `npm run dev`
3. **Run tests** — e.g., `npm test`
4. **Build** — e.g., `npm run build`
5. **Lint / format** — e.g., `npm run lint`

## Git Workflow for AI Assistants

1. Always confirm the current branch before making changes
2. Make changes on the designated feature branch
3. Stage specific files rather than `git add -A` to avoid committing secrets
4. Create a new commit (do not amend unless explicitly requested)
5. Push to remote when work is complete: `git push -u origin <branch-name>`
6. If push fails due to a network error, retry with exponential backoff (2s, 4s, 8s, 16s)

## Security Notes

- Do not commit credentials, API keys, tokens, or secrets of any kind
- `.env` files are gitignored — use `.env.example` for documenting required keys
- Review all files staged for commit before pushing

## Updating This File

Keep this file current as the project evolves. Update it when:
- A framework or build tool is added
- Test infrastructure is configured
- CI/CD pipelines are set up
- New conventions or architectural decisions are established
