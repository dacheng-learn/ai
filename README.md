# AI Agent Instructions

Reusable skills and rules for AI-assisted development.

## Setup

Add the include directive to your config file in project root:

| Tool | Config File | Include Syntax |
|------|-------------|----------------|
| Claude Code | `CLAUDE.md` | `{ai/AGENTS.md}` |
| Cursor | `.cursorrules` | Copy content or `@ai/AGENTS.md` |
| Other | `AGENTS.md` | `{ai/AGENTS.md}` |

If no config file exists, create one with the include directive.

## Structure

```
ai/
├── AGENTS.md            # Main entry point (include this)
├── rules/               # Always-applied rules
│   ├── language-rules.md
│   └── output-style.md
└── skills/              # Task-specific skills
    ├── commit-message/
    ├── develop-feature/
    ├── fix-bug/
    └── review-code/
```

## Available Skills

| Skill | Triggers |
|-------|----------|
| `commit-message` | commit message, git message, write commit, generate commit |
| `develop-feature` | new feature, add feature, implement, build, create, develop |
| `fix-bug` | fix bug, resolve error, debug, troubleshoot, issue, broken, not working |
| `review-code` | review, code review, check code, PR review |
