# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

## Repository Overview

**claude-project** is a repository for Claude integration and projects. It is currently in early initialization — the codebase is being set up for Node.js/JavaScript/TypeScript development.

- **Primary Language:** JavaScript / TypeScript (Node.js ecosystem)
- **Status:** Freshly initialized; source code and tooling are not yet added
- **Git Remote:** `http://local_proxy@127.0.0.1:41409/git/omoore0814/claude-project`

## Repository Structure

```
claude-project/
├── .gitignore        # Node.js ecosystem ignores (node_modules, dist, .env, etc.)
├── README.md         # Project title and one-line description
└── CLAUDE.md         # This file
```

As development progresses, the expected structure for a Node.js project in this repo is:

```
claude-project/
├── src/              # Source code
├── tests/            # Test files
├── dist/             # Compiled output (git-ignored)
├── node_modules/     # Dependencies (git-ignored)
├── package.json      # Project metadata and scripts
├── tsconfig.json     # TypeScript configuration (if using TS)
├── .env.example      # Environment variable template (committed)
├── .env              # Actual environment variables (git-ignored)
├── CLAUDE.md         # This file
└── README.md         # Project documentation
```

## Development Workflows

### Branch Strategy

- Development branches follow the pattern: `claude/<description>-<sessionId>`
- The main branch is `main` (remote) / `master` (local default)
- Always develop on the designated feature branch; never push directly to `main`/`master` without explicit permission

### Git Workflow

```bash
# Push to a feature branch
git push -u origin <branch-name>

# Fetch a specific branch
git fetch origin <branch-name>

# Pull updates
git pull origin <branch-name>
```

### Setup (once package.json exists)

```bash
npm install          # Install dependencies
npm run dev          # Start development server (convention)
npm run build        # Build for production (convention)
npm run test         # Run test suite (convention)
npm run lint         # Run linter (convention)
```

## Key Conventions

### Environment Variables

- **Never commit `.env`** — it is git-ignored
- Provide an `.env.example` template with all required variable names (values redacted)
- Load environment variables from `.env` using `dotenv` or equivalent

### Dependencies

- Use `npm` (preferred based on `.gitignore` patterns) or `yarn`
- Pin exact versions for production dependencies; use `^` ranges for dev dependencies
- Keep `node_modules/` out of version control (already git-ignored)

### Code Style

- Follow the conventions already established in the codebase once source files are added
- Prefer TypeScript over plain JavaScript for new code (the `.gitignore` includes `*.tsbuildinfo`)
- Use ESLint and Prettier for linting and formatting (caches are git-ignored, suggesting their use)

### Ignored Paths

The `.gitignore` covers the full Node.js ecosystem, including:

| Pattern | Reason |
|---|---|
| `node_modules/` | Dependencies — install from `package.json` |
| `dist/`, `out/`, `.next/`, `.nuxt/` | Build artifacts |
| `.env`, `.env.*` | Secrets and local config |
| `*.log`, `npm-debug.log*` | Runtime logs |
| `coverage/`, `.nyc_output` | Test coverage output |
| `.eslintcache`, `.stylelintcache` | Linter caches |
| `.pnp.*`, `.yarn/*` | Yarn v3 PnP files |

## AI Assistant Guidelines

### What to Do

- **Read files before editing them.** Never modify code you haven't read.
- **Keep changes minimal and focused.** Only change what is directly requested.
- **Prefer editing existing files** over creating new ones.
- **Commit with clear, descriptive messages** that explain *why*, not just *what*.
- **Push to the designated feature branch** (pattern: `claude/<description>-<sessionId>`).
- **Confirm before destructive actions** (deleting files, force-pushing, dropping data).

### What Not to Do

- Do not push to `main`/`master` without explicit permission.
- Do not commit `.env` files or secrets.
- Do not add unnecessary abstractions, helpers, or over-engineering.
- Do not add comments, docstrings, or type annotations to code you didn't change.
- Do not introduce security vulnerabilities (SQL injection, XSS, command injection, etc.).
- Do not retry failing commands in loops — diagnose the root cause instead.

### Security

- Validate all user input at system boundaries.
- Never expose secrets in code, logs, or commit messages.
- Use environment variables for all credentials and API keys.
- Follow OWASP top-10 guidelines when writing web-facing code.

## Current State Notes

This repository was initialized on 2026-03-19 with a single "Initial commit" containing only `.gitignore` and `README.md`. When new files and tooling are added, update this CLAUDE.md to reflect:

- The actual framework and build toolchain being used
- Real npm scripts from `package.json`
- Test runner and how to run tests
- CI/CD pipeline details
- Deployment process
- Any project-specific coding conventions
