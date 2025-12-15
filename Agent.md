# Agent

## Global Rules (always applied)

{agent/global/language-rule.md}

{agent/global/output-style.md}

## Prompt Dispatcher (applied based on intent)

Each prompt in `agent/prompts/` has frontmatter metadata:

```yaml
---
description: What this prompt does
triggers:
  - keyword1
  - keyword2
---
```

**Dispatch logic:**
1. Parse all `agent/prompts/*.md` files and extract frontmatter
2. Match user request against `triggers` (case-insensitive, partial match)
3. If matched, attach the prompt content (excluding frontmatter) to the request
4. If no match, proceed without additional prompt

**Available prompts:**

| Prompt | Description | Triggers |
|--------|-------------|----------|
| {agent/prompts/git-message.md} | Generate git commit message | commit message, git message, write commit |
| {agent/prompts/fix-bug.md} | Fix bugs with root cause analysis | fix bug, debug, troubleshoot, broken, not working |
| {agent/prompts/develop-feature.md} | Design and implement features | new feature, implement, build, create, develop |
