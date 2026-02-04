# Vibecode Blueprint

A collaborative development framework for human-AI partnership in software development. This blueprint defines the **Vibecoding** methodology—a structured approach where humans and AI work together with clear role definitions, responsibilities, and workflows.

## What is Vibecoding?

Vibecoding is a development methodology that establishes clear boundaries and protocols for AI-assisted software development:

- **AI writes code**, humans push code
- **AI prepares tests**, humans execute tests
- **AI proposes**, humans decide
- **AI suggests**, humans install dependencies

This separation ensures human oversight while leveraging AI capabilities for implementation.

## Project Structure

```
vibecode-blueprint/
├── VIBECODE_PROCEDURE.md      # Core methodology (REQUIRED for AI)
├── README.md                  # This file
└── vibecode/
    ├── PROJECT_CONTEXT.md     # AI onboarding template
    ├── PROGRESS_LOG.md        # Session & progress tracking
    └── DECISIONS.md           # Architecture decision log
```

## Getting Started

### Step 1: Load the Procedure into AI

**This is the most important step.** The `VIBECODE_PROCEDURE.md` file contains all the rules and workflows that the AI must follow.

**Option A: Paste into AI context**
Copy the entire contents of `VIBECODE_PROCEDURE.md` and paste it at the start of your AI conversation.

**Option B: Add to project rules (recommended)**
If your AI tool supports project-level instructions (e.g., Claude Projects, Cursor rules, Windsurf rules), add the procedure there so it persists across sessions.

**Option C: Include in system prompt**
For API integrations, include the procedure in your system prompt.

> **Why is this required?** Without the procedure, the AI doesn't know the Vibecoding methodology—the core rules, stage-based workflow, what it must ask permission for, and how to handle git handoffs.

### Step 2: Set Up Project Templates

Copy the templates to your project root:

```bash
cp vibecode/PROJECT_CONTEXT.md PROJECT_CONTEXT.md
cp vibecode/PROGRESS_LOG.md PROGRESS_LOG.md
cp vibecode/DECISIONS.md DECISIONS.md
```

### Step 3: Configure Your Project

1. **Fill out PROJECT_CONTEXT.md** with your tech stack, architecture, and coding conventions

2. **Choose your mode** in PROGRESS_LOG.md:
   - **Solo Mode**: One human + AI
   - **Team Mode**: Multiple team members + AI

### Step 4: Start Vibecoding

With the procedure loaded and templates configured, you're ready to start developing using the stage-based workflow.

## Core Concepts

### Decision Authority Matrix

| Decision Type | AI Role | Human Role |
|--------------|---------|------------|
| Architecture & Tech Stack | Proposes options | Makes final decision |
| Dependencies | Suggests packages | Approves & installs |
| Code Implementation | Writes code | Reviews & approves |
| Git Operations | Suggests commands | Executes all git operations |
| Testing | Prepares test procedures | Executes tests, reports results |

### Stage-Based Development

Features are broken into testable stages:

```
AI Proposes → Human Approves → AI Implements →
AI Prepares Test → Human Tests → Human Pushes
```

Each stage requires human sign-off before proceeding.

### Progress Log

The Progress Log is the single source of truth that enables:
- AI model transitions (switching between AI sessions)
- Team continuity across time zones
- Clear status tracking for all stakeholders

Update it after every significant change.

## Templates

### PROJECT_CONTEXT.md
Onboard AI to your project with:
- Project overview and purpose
- Tech stack details
- Architecture and key patterns
- Coding conventions
- Environment variables
- Human preferences

### PROGRESS_LOG.md
Track development progress:
- Current status and blockers
- Session history
- Feature stage tracking
- Test results
- Handoff notes

### DECISIONS.md
Document architectural decisions:
- Context and problem statement
- Options considered
- Chosen decision and rationale
- Decision authority and date

## Workflows

### Solo Mode
```
Human (Decision Maker)
        ↓
   AI (Implementer)
        ↓
Human (Tester & Git Operator)
```

### Team Mode
```
Project Lead → defines requirements
        ↓
AI → implements code
        ↓
Code Maintainer → reviews & manages git
        ↓
Tester → executes test procedures
```

## Security Guidelines

- AI never hardcodes credentials
- Environment variables required for all secrets
- Human approval required for security decisions
- AI flags potential vulnerabilities for human review

## Quick Reference

### Starting a New AI Session

1. **Load `VIBECODE_PROCEDURE.md`** into the AI (paste or include in rules)
2. AI reads `PROJECT_CONTEXT.md` for project understanding
3. AI reads `PROGRESS_LOG.md` for current state
4. AI reads `DECISIONS.md` for architectural context
5. AI summarizes understanding, human confirms
6. Continue from documented state

### Ending a Session

1. Update Progress Log with completed work
2. Document any new decisions in DECISIONS.md
3. Note handoff items for the next session

### File Purposes

| File | Purpose | When to Use |
|------|---------|-------------|
| `VIBECODE_PROCEDURE.md` | Teaches AI the methodology | Load at start of every AI session |
| `PROJECT_CONTEXT.md` | Project-specific info | AI reads to understand your project |
| `PROGRESS_LOG.md` | Current state & history | AI reads/updates during development |
| `DECISIONS.md` | Architecture decisions | AI reads for context, updates when decisions made |

## Contributing

This is a template project. Feel free to:
- Adapt the templates to your team's needs
- Modify the workflow to fit your process
- Add additional templates as needed

## License

This project is open for use and adaptation.
