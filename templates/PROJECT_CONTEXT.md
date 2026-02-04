# Project Context

> **Purpose:** Essential information for AI onboarding. New AI reads this to understand the project.

---

## Overview

**Project Name:** [Name]
**Description:** [2-3 sentences about what this project does]
**Status:** [Planning / In Development / Production]

---

## Tech Stack

| Layer | Technology | Version |
|-------|------------|---------|
| Language | [e.g., TypeScript] | [e.g., 5.0] |
| Framework | [e.g., Next.js] | [e.g., 14.0] |
| Database | [e.g., PostgreSQL] | [e.g., 15] |
| ORM | [e.g., Prisma] | [e.g., 5.0] |
| Deployment | [e.g., Vercel] | - |

---

## Architecture

### Structure
```
project-root/
├── src/
│   ├── [folder]/     # [purpose]
│   └── [folder]/     # [purpose]
├── tests/
└── config/
```

### Key Patterns
- **[Pattern]:** [When/how to use it]
- **[Pattern]:** [When/how to use it]

### Critical Files (Don't Modify Without Approval)
| File | Purpose | Risk |
|------|---------|------|
| `src/config/` | Configuration | High |
| `src/models/` | Database schemas | High |
| `.env*` | Secrets | Critical |

---

## Coding Conventions

- **Naming:** [e.g., camelCase for functions, PascalCase for components]
- **Files:** [e.g., kebab-case.ts]
- **Error handling:** [Approach used]

---

## Environment Variables

| Variable | Purpose | Required |
|----------|---------|----------|
| `DATABASE_URL` | Database connection | Yes |
| `API_KEY` | External API | Yes |

> Never commit actual values. Use `.env.example` for reference.

---

## Human Preferences

> Things the human prefers (for AI to follow)

- [e.g., Detailed error messages]
- [e.g., Use Zod for validation]
- [e.g., Prefer functional components]

---

## Known Limitations / Tech Debt

- [ ] [Issue to address later]
- [ ] [Issue to address later]

---

*Last updated: [Date]*