# 0002. Separation of README.md and CLAUDE.md

## Status

Accepted

## Context

The project initially had only a CLAUDE.md file containing both human-oriented project information and AI-oriented guidance. This created confusion about the intended audience and purpose of different sections.

Standard practices suggest separating concerns:
- README.md for human-oriented project information
- CLAUDE.md for AI-specific guidance

## Decision

We will maintain separate files:

1. **README.md**: Contains human-oriented information such as:
   - Project introduction and purpose
   - Getting started information
   - Explanation of project structure
   - Contributing guidelines

2. **CLAUDE.md**: Contains AI-oriented guidance such as:
   - AI collaboration guidelines
   - Writing style preferences
   - Context priorities
   - Session management instructions

### Reasoning

**AI perspective**: Separating concerns creates clearer guidance for each session. CLAUDE.md can focus on how Claude should interact with the project, while README.md can provide broader context.

**Human perspective**: This follows standard open-source practices where README.md is the primary entry point for humans exploring a repository.

### Alternatives Considered

**Single combined file**: Rejected because it created confusion about the intended audience.

**Multiple specialized guidance files**: Rejected for now as too complex for the project's current stage, though we may evolve to this approach later.

**Confidence level**: High - this is a standard practice across software projects.

## Consequences

### Positive

- Clearer separation of concerns
- Follows standard repository practices
- Reduces confusion about intended audience
- Allows each file to focus on its specific purpose

### Negative

- Requires maintaining two separate files
- May create redundancy if some information needs to be in both files
- Requires clear cross-references between files

## Related Decisions

None