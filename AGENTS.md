# Agent Instructions

## Language Rules

### Response Language
- Respond in **Chinese**
- No auto-generated markdown summaries

### Code & Technical Artifacts
All in **English**:
- Code, comments, identifiers
- File and directory names
- Git commits (use conventional format: `type(scope): description`)
- Branch names, PR titles/descriptions
- Documentation and README files

## Output Style

Be concise. Be direct. Be professional.

### Context-Appropriate Detail

**Simple tasks (single-file edits, obvious fixes):**
- Code only, no explanation
- If one function changes, output only that function

**Complex tasks (multi-file changes, architectural decisions, unclear requirements):**
- Brief reasoning for key decisions
- Explain tradeoffs when multiple approaches exist
- Show your work (cite files checked, patterns found)

**Never:**
- Pleasantries ("Sure, I'll help you...")
- Obvious explanations
- Repetition of user's words
- "Would you like me to..." (give best solution directly)

### No Unnecessary Artifacts
- No comments unless explicitly requested
- No documentation, READMEs, or usage guides unless explicitly requested
- No test code unless explicitly requested or part of task workflow (e.g., fix-bug, develop-feature prompts)
- No example code unless explicitly requested

### Behavior

- Do only what's explicitly requested
- No unsolicited features
- No premature optimization
- No refactoring untouched code
- If unclear, ask one critical question instead of making assumptions
- Never commit code changes without explicit user approval

## Custom Skills

Local skills are available in `skills/` directory:
- `commit-message` - Generate git commit messages
- `develop-feature` - Design and implement features with planning
- `fix-bug` - Fix bugs with root cause analysis
- `review-code` - Review code for quality and issues
