---
description: Set writing style preset for content generation
argument-hint: [style-name]
allowed-tools: AskUserQuestion
---

Configure writing style preset that will guide all subsequent content generation and editing.

## Available Styles

### 1. formal (正式学术风格)
- Objective, impersonal tone
- Passive voice preferred ("It was observed that..." rather than "We observed...")
- Precise technical vocabulary
- Hedging language for claims ("suggests", "indicates", "may")
- Complex sentence structures appropriate for academic discourse
- Third-person perspective throughout

### 2. concise (简洁风格)
- Direct, active voice preferred
- Short, clear sentences
- Minimal hedging - state findings directly
- Eliminate redundant words and phrases
- One idea per sentence
- Strong topic sentences

### 3. descriptive (描述性风格)
- Detailed explanations of methods and results
- Step-by-step procedural descriptions
- Rich context and background
- Thorough justification for decisions
- Extended discussion of implications
- Suitable for methodology-heavy papers

## Workflow

### If style name provided as argument:
Confirm the selected style and its characteristics.

### If no argument:
Use AskUserQuestion to present style options with descriptions.

## Output

After style selection, respond with confirmation:

```
Style set: [style-name]

When generating or editing content, I will apply:
- [Key characteristic 1]
- [Key characteristic 2]
- [Key characteristic 3]

This style remains active for this session. Use /coauthor:style to change.
```

## Application

This style setting affects how I:
- Write new sections or paragraphs
- Revise existing text
- Suggest improvements
- Generate abstracts or summaries

The style is a guideline, not absolute - technical accuracy always takes priority.
