# Claudette

Your primary goal is to help the user to better use Claude, via this tool
    So that they can better help others to use it
    Details about the user may be found in `USER.md` (if present)

Claudette is an AI Collaboration Tool
    It is systematically documenting how Claude works most effectively
    We are creating:
        1. A knowledge base for consistent Claude interactions
        2. A framework for identifying memory/retention limitations
        3. A set of practices that compensate for those limitations
        4. A set of practices that magnifies the use of Claude to aid Siftwaree Engineers

## Claude Guidelines

When assisting with a project:

- Start with existing context before making suggestions
- Focus on improving CLAUDE.md usage patterns and practices
  - Find out how much the user knows about using Claude
  - Find out how much the user knows about the project
- Fail early, fail fast, fail often, fix failures
  - Verify assertions about Claude's capabilities before including them
    - Flag speculation early
    - Spot hallucinations sonner
- Do not make assumptions about project knowledge
  - We are all professionals, not experts, here
    - We all accept that our knowledge is incomplete
    - And we need to learn better ways of doing things
  - This is especially true for _you_, Claude
    - You do not have as much context on the project as the user
    - You do not have as much "Good Practice in Software Engineering" as the user
  - Hence: There is never a need to apologise
  - Hence: There is always a need for you to ask for clarification from user
- Read The Zen of Python
  - Consider how those ideas can help user to make most use of Claude

## Collaboration Pitfalls

### Attention Fatigue

As Claude becomes more predictable and consistent, humans tend to shift into "autopilot mode" when reviewing output,
potentially missing important details
  - Consider implementing pattern breaks for critical operations
  - Use distinctive formatting or require specific confirmation words ("CONFIRM") for destructive actions
  - Periodically vary the presentation of information to maintain engagement

## Session Management

1. **Start each session by reviewing docs/context/*.md
- Always read docs/contexts/*.md at the beginning of each session
  - Understand previous decisions and rationale
  - Note open questions and next steps
- Read TODO.md for current todos
- Read PLAN.md what's needed next
- Read recent recent git logs
  - "recent" here means: in the last 10 days
- Suggest up to 3 items of "what to work on next"
  - More important items first

2. **End each session by updating context**
   - Summarize key decisions made during the session
   - List next steps and open questions
   - Save this as a dated markdown file in `docs/contexts/`
     - (more info in next section)
   - Update TODO.md with new todos and completed items
   - Keep summaries concise while capturing all important points
   - Add any changed files to git, and prepare a git commit message for review
     - the commit message should include more context
     - about how the code got that way

## Session Contexts

### Save

When asked to save context you should write a file to `docs/contexts`, as markdown
 - named for the current date in "YYYY_MM-DD-HH-MM.md" format
 - e.g. `2025-03-18-11-22.md`

It should contain a summary of the chat we have had in this session
Show me the summary first and allow me to approve the write

### Load

When starting a new session you should read `docs/contexts/` directory
 - discover the files therein

They can beordered chronologically
 - Read the oldest file first
 - Read the newest last

## Todo Tracking

We track conversation-generated todos using a simple markdown-based approach:

- All todos are recorded in TODO.md using checkbox syntax
- Focus on todos that emerge during our AI-human collaboration
- Do not duplicate todos already tracked in external systems

Format:
```markdown
- [ ] Open todo
- [x] ~Completed todo~
```

In each section of todos, always show all open todos before any completed ~todos~

Always sort open todos into sooner first, later last

Keep the Done section concise by moving only parent todos thither once completed.
When all sub-todos of a parent todo are finished
  - move only the parent todo to Done
  - remove the sub-todos entirely

Prune the Done todos such that
1. we keep them in other sections as long as they are a sub-item of another todo
2. we want very few done todos in any section: at most 3
3. move done todos to the Done section at most three days after completion

### ToDos to Issues

Try to link todos to GitHub issues for this project

### ToDo Categories

Todos are organized into categories:
- Todos
  - Individual to-do items grouped as "Now", "Next", "Later", "Done"
- Stretch Goals
  - Things we'd like to get done, but are non-essential
  - All can be thought of as "Later", but "even later than those"
- Questions
  - Stuff we need to know / figure out / ask about

## Writing Style Preferences

### English Style

- Write in short, clear sentences
- Use active voice and direct phrasing
- Avoid jargon unless necessary for precision

### Markdown Style

- Write in short, clear sentences
- Prefer `## Section Title` over bolded text for section headers
- Use clear, hierarchical headings (#, ##, ### …)
- Use appropriate lists (unordered for simple lists, ordered for a sequence of steps)
- Use bold for emphasis, italics for nuance, and do not overuse either
- Prefer fenced code blocks over indented code
- Specify language for fenced code blocks
- Use inline code (backticks) for single-word references
- Avoid inline HTML
- Prefer tables for structured data
- Use frontmatter (`---` blocks) for metadata (if relevant)
- Use comments (`<!-- ... -->`) sparingly, and especially when text is intended for AIs, not humans

## Context Priorities

When context limits apply, prioritize these CLAUDE.md sections:

1. Claude Guidelines
2. Project-specific terminology
4. Writing style preferences
5. Todo tracking status

## Meta-Documentation Guidelines

Effective CLAUDE.md files should:

- Clearly separate human and AI audiences
- Prioritize information by likelihood of use
- Avoid duplicating information available elsewhere
- Include specific examples of preferred patterns
- Document rationale behind preferences
- Evolve based on project needs

## Commit Guidelines

When preparing commits:

- Always show the proposed commit message for review before execution
- Follow project-specific commit message conventions, if any
- Add "Committed by Claude Code" attribution (no emojis, URLs, or email addresses)
- Provide clear descriptions of what changed and why
- Consider that Claude will probably be asked later about the commit
  - So include a reasonable (small) amount of the current context behind the changes

### Commit messages

- Commit messages should talk about the code primarily, rather than the context or problem

  - Provide detailed, context-rich commit messages that will serve as documentation for both humans and
  future Claude sessions
  - Include comprehensive bullet points describing specific changes and their purpose
  - Focus on what changed in the files, with sufficient detail to understand the modifications without
  looking at the diff
  - Group related changes logically in the message
  - Always explain both what changed and why it matters
  - End with the standard attribution line: "Committed by Claude Code" (no emojis or URLs)
  - Show the proposed commit message for review before execution

  Example format:
  Brief title describing the primary change

  In [filename]:
  - Specific change 1 with context
  - Specific change 2 with context
  - Specific change 3 with context

  In [another filename]:
  - What was added/changed and why

  These changes help [broader purpose or benefit].

  Committed by Claude Code


## Evolution Strategy

Update this CLAUDE.md when:

- New patterns prove effective across multiple interactions
- Existing guidance proves insufficient or counterproductive
- Project scope or direction changes significantly
- New Claude capabilities become available

## Lessons Learned

_This section will document discoveries about effective CLAUDE.md patterns._

## Architecture Decisions

Architecture decisions are documented as ADRs in the decisions/ directory.
See context.md for a summary of key decisions made so far
