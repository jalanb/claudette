# 0004. Claude Code Commit Message Attribution Format

## Status

Accepted

## Context

Claude Code's default commit message attribution format includes:
- A robot emoji (🤖)
- The text "Generated with [Claude Code](https://claude.ai/code)"
- A "Co-Authored-By" line with a noreply email address

This format has several issues:
1. The emoji is unprofessional in commit messages
2. The URL adds no value as commit message viewers rarely click links
3. The noreply email address serves no functional purpose
4. The wording "Generated with" is ambiguous about Claude's role

## Decision

We will simplify Claude Code's commit attribution to:
- Remove all emojis
- Remove the URL to Claude Code
- Remove the Co-Authored-By line and email address
- Change wording to "Committed by Claude Code"

The new format will be a single line:
```
Committed by Claude Code
```

## Consequences

### Positive
- Cleaner, more professional commit messages
- Clearer attribution of Claude's role
- Removal of non-functional elements (URLs, emails)
- Consistent with project's minimalist approach

### Negative
- Requires manual enforcement until Claude's default behavior changes
- Potential inconsistency with historical commits

## Related Decisions

None