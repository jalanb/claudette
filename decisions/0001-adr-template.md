# 0001. Custom ADR Template for AI-Human Collaboration

## Status

Accepted

## Context

This project needs a mechanism to document decisions made during AI-human collaboration. Standard ADR templates focus primarily on technical architecture decisions and don't capture the nuanced aspects of AI-human interactions.

## Decision

We will use a custom ADR template that includes:

```markdown
# [ADR Number]. [Title]

## Status

[Proposed, Accepted, Deprecated, Superseded]

## Context

[Background and problem statement, including:
- Original question or challenge
- Constraints that influenced the decision
- Previous approaches (if any)]

## Decision

[The decision made, including:
- Reasoning from both AI and human perspectives
- Alternatives considered and why they were rejected
- Confidence level in this decision]

## Consequences

[Results of applying the decision, including:
- Positive outcomes
- Negative outcomes
- Open questions or risks
- Impact on future decisions]

## Related Decisions

[References to other ADRs that influenced or are influenced by this one]
```

This template extends the standard ADR format to better capture AI-human collaboration patterns.

## Consequences

### Positive

- Captures both AI and human reasoning
- Documents alternatives considered (negative information)
- Includes confidence levels to reflect uncertainty
- Maintains connections between related decisions

### Negative

- Slightly more verbose than standard ADRs
- Requires discipline to maintain consistently
- May evolve as we learn more about effective AI-human collaboration

## Related Decisions

None (this is the first ADR)