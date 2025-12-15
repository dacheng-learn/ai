# Agents

## Global Rules (always applied)

{agents/global/language-rules.md}

{agents/global/output-style.md}

## Prompt Dispatcher (applied based on intent)

Each prompt in `agents/prompts/` has frontmatter metadata:

```yaml
---
description: What this prompt does
triggers:
  - keyword1
  - keyword2
---
```

**Dispatch logic:**
1. Parse all `agents/prompts/*.md` files and extract frontmatter
2. Match user request against `triggers` (case-insensitive, partial match)
3. If matched, attach the prompt content (excluding frontmatter) to the request
4. If no match, proceed without additional prompt

**Available prompts:**

| Prompt | Description | Triggers |
|--------|-------------|----------|
| {agents/prompts/develop-feature.md} | Design and implement features | new feature, add feature, implement, build, create, develop |
| {agents/prompts/fix-bug.md} | Fix bugs with root cause analysis | fix bug, resolve error, debug, troubleshoot, issue, broken, not working |
| {agents/prompts/review-code.md} | Review code for quality and issues | review, code review, check code, PR review |
| {agents/prompts/commit-message.md} | Generate git commit message | commit message, git message, write commit, generate commit |
