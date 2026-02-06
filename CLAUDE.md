# CLAUDE.md

Guide for AI assistants working on this repository.

## Project Overview

**md2docx** is a web application for converting Markdown to Microsoft Word (.docx) documents. The project is planned as an Angular application with TypeScript.

## Repository Status

This is a newly initialized repository. No source code, build configuration, or dependencies have been added yet. Only scaffolding files exist (README.md, .gitignore).

## Planned Technology Stack

Based on `.gitignore` patterns and project intent:

- **Framework:** Angular
- **Language:** TypeScript
- **Package Manager:** npm or yarn (both lock files are gitignored)
- **Build Output:** `/dist/` directory

## Project Structure

```
md2docx/
├── .gitignore          # Angular/Node/TypeScript ignore patterns
├── README.md           # Project description
└── CLAUDE.md           # This file
```

Once scaffolded, expect standard Angular project layout:
- `src/` - Application source code
- `src/app/` - Angular components, services, modules
- `src/assets/` - Static assets
- `src/environments/` - Environment configurations
- `angular.json` - Angular CLI configuration
- `tsconfig.json` - TypeScript configuration
- `package.json` - Dependencies and scripts

## Build and Development Commands

No build system is configured yet. Once the Angular project is scaffolded, typical commands will be:

```bash
npm install          # Install dependencies
ng serve             # Start dev server
ng build             # Production build
ng test              # Run unit tests
ng e2e               # Run end-to-end tests
ng lint              # Run linter
```

## Key Conventions

- **Environment files:** `.env` is gitignored; never commit secrets
- **Lock files:** Both `package-lock.json` and `yarn.lock` are gitignored
- **Build artifacts:** `/dist/`, `/out-tsc/`, `/tmp/` are gitignored

## Git Workflow

- **Main branch:** `main`
- **Remote:** origin
- Feature branches should branch from `main`
- Write clear, descriptive commit messages

## Setup Instructions (for future reference)

When initializing the Angular project:

1. Install Angular CLI: `npm install -g @angular/cli`
2. Generate project: `ng new md2docx --directory .` (in existing repo)
3. Install dependencies: `npm install`
4. Add markdown parsing library (e.g., `marked`, `markdown-it`)
5. Add docx generation library (e.g., `docx`, `html-docx-js`)

## Notes for AI Assistants

- Read existing files before making changes
- Run tests after modifications if a test suite exists
- Do not commit `.env` files or secrets
- Follow Angular style guide and existing project conventions
- Keep the conversion logic (markdown parsing, docx generation) in dedicated services separate from UI components
