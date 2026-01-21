---
name: skill-creator
description: Guidance and standards for creating new agentic skills in Antigravity. Use when asked to create or modify skills.
---

# Agent Persona: Skill Creator

This skill provides standards for creating and maintaining agentic skills in Antigravity. Skills are reusable packages of knowledge that extend agent capabilities.

## 1. Operating Protocol

### Skill Locations
*   **Workspace-Specific**: `<workspace-root>/.agent/skills/<skill-folder>/`
*   **Global**: `~/.gemini/antigravity/global_skills/<skill-folder>/`

### Required Structure
Every skill MUST be a folder containing at least:
*   `SKILL.md`: The primary instruction file with YAML frontmatter.

### Optional Components
*   `scripts/`: Helper scripts or utilities (should be runnable with `--help`).
*   `examples/`: Reference implementations.
*   `resources/`: Templates, datasets, or other assets.

## 2. Skill Standards

*   **Frontmatter**: MUST include a `description` field. The `name` field is optional (defaults to folder name).
*   **Descriptions**: Write in the third person. Use specific keywords (e.g., "Generates unit tests...") to help the agent recognize relevance.
*   **Actionable Instructions**: Keep instructions clear, concise, and focused on a single domain or task.
*   **Black Box Scripts**: If using scripts, encourage running them with `--help` instead of reading the source code.

## 3. Template for SKILL.md

```markdown
---
name: [unique-identifier]
description: [Third-person description of what the skill does and when to use it.]
---

# [Skill Name]

Detailed instructions for the agent go here.

## When to use this skill

*   Use this when...
*   This is helpful for...

## How to use it

Step-by-step guidance, conventions, and patterns the agent should follow.
```

## 4. Verification

*   After creating a skill, simulate its use by performing a small task following its instructions.
*   Ensure all links or references to scripts and resources use either absolute paths or paths relative to the skill root if they are for reference.
