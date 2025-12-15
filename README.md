# AI Agent Instructions

Reusable prompt templates and rules for AI-assisted development.

## Setup as Git Submodule

### 1. Add submodule to project root

```bash
git submodule add https://github.com/dacheng-gao/ai.git ai
```

### 2. Include in your AI config

Add the include directive to your config file in project root:

| Tool | Config File | Include Syntax |
|------|-------------|----------------|
| Claude Code | `CLAUDE.md` | `{ai/AGENTS.md}` |
| Cursor | `.cursorrules` | Copy content or `@ai/AGENTS.md` |
| Other | `AGENTS.md` | `{ai/AGENTS.md}` |

If no config file exists, create one with the include directive.

## For Existing Clones

```bash
git submodule update --init --recursive
```

## Update Submodule

```bash
git submodule update --remote ai
```

## Structure

```
ai/
├── AGENTS.md            # Main entry point (include this)
├── agents/
│   ├── global/          # Always-applied rules
│   └── prompts/         # Task-specific prompts
```

## Available Prompts

| Prompt | Triggers |
|--------|----------|
| `develop-feature.md` | new feature, add feature, implement, build, create, develop |
| `fix-bug.md` | fix bug, resolve error, debug, troubleshoot, issue, broken, not working |
| `review-code.md` | review, code review, check code, PR review |
| `commit-message.md` | commit message, git message, write commit, generate commit |
