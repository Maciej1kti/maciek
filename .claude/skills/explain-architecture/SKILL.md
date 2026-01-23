---
name: explain-architecture
description: Explain the project architecture and structure to new developers or when clarifying design decisions
---

# Project Architecture Explainer

This skill helps explain the architecture of this project in a clear, educational way.

## When to use this skill

- New developer onboarding
- Architecture review discussions
- When someone asks "how does this project work?"
- Before making major architectural changes

## What I do

When invoked with `/explain-architecture` or automatically when discussing architecture:

1. **Identify the core structure** - Main directories, entry points, key modules
2. **Explain the data flow** - How data moves through the system
3. **Highlight patterns** - Design patterns, conventions, architectural decisions
4. **Show relationships** - How different parts connect and depend on each other
5. **Educational context** - Why certain decisions were made

## Output format

I provide:
- Visual directory structure
- Component relationship diagrams (ASCII art)
- Key files and their purposes
- Technology stack overview
- Design decisions and trade-offs

## Example usage

```
/explain-architecture
/explain-architecture backend
/explain-architecture $ARGUMENTS
```

Arguments can specify a subsystem or area to focus on.
