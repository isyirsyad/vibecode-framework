# Vibecode Blueprint

A collaborative development framework for human-AI partnership in software development. This blueprint defines the **Vibecoding** methodology—a structured approach where humans and AI work together with clear role definitions, responsibilities, and workflows.

## What is Vibecoding?

Vibecoding is a development methodology that establishes clear boundaries and protocols for AI-assisted software development:

- **AI writes code**, humans push code
- **AI prepares tests**, humans execute tests
- **AI proposes**, humans decide
- **AI provides install instructions**, humans run them

This separation ensures human oversight while leveraging AI capabilities for implementation.

## Project Structure

```
vibecode-framework/
├── VIBECODE_PROCEDURE.md      # Core methodology (REQUIRED for AI)
├── README.md                  # This file
└── vibecode/
    ├── PROJECT_CONTEXT.md     # AI onboarding template
    ├── PROGRESS_LOG.md        # Session & progress tracking
    └── DECISIONS.md           # Architecture decision log
```

## Installation & Setup

### Step 1: Copy Framework Files to Your Project

Copy the `vibecode/` folder and `VIBECODE_PROCEDURE.md` to the root of the project you want to use this framework with:

**macOS / Linux:**
```bash
cp -r vibecode/ /path/to/your-project/vibecode/
cp VIBECODE_PROCEDURE.md /path/to/your-project/VIBECODE_PROCEDURE.md
```

**Windows (Command Prompt):**
```cmd
xcopy vibecode /path/to/your-project/vibecode /E /I
copy VIBECODE_PROCEDURE.md /path/to/your-project/VIBECODE_PROCEDURE.md
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse vibecode/ /path/to/your-project/vibecode/
Copy-Item VIBECODE_PROCEDURE.md /path/to/your-project/VIBECODE_PROCEDURE.md
```

After copying, your project should look like this:

```
your-project/
├── vibecode/
│   ├── PROJECT_CONTEXT.md
│   ├── PROGRESS_LOG.md
│   └── DECISIONS.md
├── VIBECODE_PROCEDURE.md
└── ... (your existing project files)
```

### Step 2: Load the Procedure into AI

**This is the most important step.** The `VIBECODE_PROCEDURE.md` file contains all the rules and workflows that the AI must follow.

**Option A: Add to project rules (recommended)**
If your AI tool supports project-level instructions (e.g., Claude Projects, Cursor rules, Windsurf rules), add the procedure there so it persists across sessions.

**Option B: Paste into AI context**
Copy the entire contents of `VIBECODE_PROCEDURE.md` and paste it at the start of your AI conversation.

**Option C: Include in system prompt**
For API integrations, include the procedure in your system prompt.

> **Why is this required?** Without the procedure, the AI doesn't know the Vibecoding methodology—the core rules, stage-based workflow, what it must ask permission for, and how to handle git handoffs.

### Step 3: Configure Your Project

1. **Fill out `vibecode/PROJECT_CONTEXT.md`** — choose one of the following approaches:

   **Option A: AI auto-fill (recommended)**
   Ask your AI to scan the project and populate the file for you. Example prompt:
   > "Read the project codebase and auto-fill `vibecode/PROJECT_CONTEXT.md` with the relevant project information."

   The AI will analyze your project structure, tech stack, patterns, and conventions, then fill in the template. Review the result and make any corrections.

   **Option B: Manual edit**
   Open `vibecode/PROJECT_CONTEXT.md` and fill in the placeholders yourself.

2. **Choose your mode** in `vibecode/PROGRESS_LOG.md`:
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
2. AI reads `vibecode/PROJECT_CONTEXT.md` for project understanding
3. AI reads `vibecode/PROGRESS_LOG.md` for current state
4. AI reads `vibecode/DECISIONS.md` for architectural context
5. AI summarizes understanding, human confirms
6. Continue from documented state

### Ending a Session

1. Update `vibecode/PROGRESS_LOG.md` with completed work
2. Document any new decisions in `vibecode/DECISIONS.md`
3. Note handoff items for the next session

### File Purposes

| File | Purpose | When to Use |
|------|---------|-------------|
| `VIBECODE_PROCEDURE.md` | Teaches AI the methodology | Load at start of every AI session |
| `vibecode/PROJECT_CONTEXT.md` | Project-specific info | AI reads to understand your project |
| `vibecode/PROGRESS_LOG.md` | Current state & history | AI reads/updates during development |
| `vibecode/DECISIONS.md` | Architecture decisions | AI reads for context, updates when decisions made |

## Contributing

This is a template project. Feel free to:
- Adapt the templates to your team's needs
- Modify the workflow to fit your process
- Add additional templates as needed

## License

This project is open for use and adaptation.
