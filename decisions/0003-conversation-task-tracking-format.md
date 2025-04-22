# 0003. Conversation-Based Task Tracking Format

## Status

Proposed

## Context

During our AI-human collaboration sessions, we frequently identify tasks that need tracking. These are specifically:

- Tasks that emerge organically during conversation
- Day-to-day implementation details not captured in external systems
- Follow-up items specific to CLAUDE.md refinement

We need a lightweight format to capture these conversation-generated tasks without duplicating external tracking systems (like Jira or GitHub Issues).

## Decision

We will use a TODO.md file with markdown checkbox syntax to track conversation-generated tasks:

```markdown
- [ ] Open task
- [x] Completed task
```

This format was chosen over alternatives like:
- GitHub Issues (rejected due to vendor lock-in and separation from documentation)
- Taskwarrior-style formats (rejected due to poor readability)
- TiddlyWiki/Obsidian (rejected as requiring external tools)
- Inline code comments (rejected as this is primarily documentation, not code)

## Consequences

### Positive
- Simple, readable plain text format that complements our markdown documentation
- Clear visual distinction between completed and pending items
- Maintains conversation context that might be lost in external systems
- No external dependencies

### Negative
- No integration with external task systems
- Requires manual maintenance
- Limited filtering/sorting capabilities
- Potential for divergence from official project tracking

## Related Decisions

- 0002-documentation-separation.md (This task format complements our documentation approach)