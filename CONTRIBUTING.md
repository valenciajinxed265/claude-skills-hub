# Contributing to Claude Skills Hub

Thanks for your interest in contributing! This is a community-driven collection, and we welcome new skills from everyone.

## How to Add a New Skill

1. **Fork** this repository
2. **Choose** the right category folder under `skills/`
3. **Create** a `.md` file with this format:

```markdown
---
description: Short description of what this skill does
allowed-tools: Read, Edit, Write, Glob, Grep, Bash
---

Your detailed prompt here...
```

4. **Submit** a Pull Request with:
   - Clear title: `Add [skill-name] to [category]`
   - Brief description of what the skill does
   - Example use case

## Skill Guidelines

- **Be specific** - Generic skills are less useful than focused ones
- **Be thorough** - Include step-by-step instructions, edge cases, and best practices
- **Be practical** - Skills should solve real problems developers face daily
- **Test your skill** - Try it in Claude Code before submitting
- **Follow conventions** - Use kebab-case for filenames, include all frontmatter fields

## Suggesting a Category

If your skill doesn't fit any existing category, open an issue to discuss adding a new one.

## Reporting Issues

- **Broken skill?** Open an issue with the skill name and error details
- **Improvement idea?** Open an issue or PR with your suggested changes

## Code of Conduct

Be respectful, constructive, and inclusive in all interactions.
