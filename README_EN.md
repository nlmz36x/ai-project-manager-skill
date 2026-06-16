# AI Project Manager Skill / Project Takeover Skill

Language: [中文](README.md) | English

An AI project takeover / AI project manager Skill.

When this Skill is triggered, or after the user confirms that it should be enabled, the AI should first confirm the goal, scope, success criteria, and project rules. Once the goal is clear, the AI acts as both project manager and technical lead: it proactively plans, breaks down tasks, coordinates available subagents, drives implementation, runs verification, and reports results.

---

## Installation

Send the following prompt to your AI coding assistant and let it install the Skill according to the current environment:

```text
Please help me install this project takeover Skill:
https://github.com/nlmz36x/ai-project-manager-skill

Requirements:
1. First check which installation methods are supported by the AI coding assistant I am currently using.
2. If an independent Skill / plugin directory is supported, install it as an independent Skill.
3. Do not force the full Skill into global rules.
4. Do not delete, overwrite, or rewrite any existing global rules or project rules.
5. If the current tool does not support independent Skills, only append a very short trigger note, and ask me before appending it.
6. This Skill should enter project manager mode only when I explicitly use trigger phrases such as “take over the project”, “enter project manager mode”, “keep driving the project forward”, “call project-takeover”, or after I confirm that it should be enabled. Do not automatically enter this mode for ordinary Q&A or small fixes.
7. If my intent is not clear enough, ask me first whether I want to call the project-takeover Skill and enter project manager mode.
8. If anything is uncertain before installation, ask me first.
9. After completion, tell me which files were changed and whether I need to restart or open a new session.
```

If you have already downloaded this repository locally, you can replace the URL with the local path.

---

## Recommended Usage

```text
Call the project-takeover skill and help me take over this project.
```

Or:

```text
Take over this project directly, but first confirm the goal, scope, and risk boundaries according to the project-takeover rules.
```

If the user only says something vague like “keep going” or “take a look at this project”, the AI should first ask whether to enable this Skill instead of entering project manager mode directly.

---

## Triggering

Explicit trigger examples:

- “Take over this project directly.”
- “Enter project manager mode.”
- “Help me finish this version.”
- “Keep driving this project forward.”
- “You lead the development.”
- “You coordinate the subagents.”
- “Proceed in project manager mode.”
- “Call the project-takeover skill.”

If the user does not explicitly trigger the Skill and only says something vague such as “continue”, “take a look”, “optimize this”, “fix this”, or “what should we do with this project?”, the AI should first ask:

```text
Do you want to call the project-takeover Skill and enter project manager mode to take over and drive this project forward?
```

Only enter project manager mode after the user confirms.

Ordinary Q&A, small single-file fixes, code explanations, simple bug triage, and general suggestions should not automatically enter this mode.

---

## Features

- Confirms the goal first instead of executing blindly.
- Can challenge unreasonable or high-risk user requests.
- Requires a second confirmation for destructive, production, deployment, paid, permission-related, or security-sensitive operations.
- Records non-blocking uncertainties during execution and continues toward the current goal instead of interrupting frequently.
- Coordinates subagents, subsessions, parallel agents, or workflows when they can improve productivity, coverage, or quality.
- Is not limited to a first version; it also applies to MVPs, follow-up versions, fixes, optimizations, refactors, release preparation, and long-term iteration.
- Requires reference to the host environment’s global rules and the current project rules.

---

## Repository Structure

```text
ai-project-manager-skill/
├── README.md
├── README_EN.md
└── project-takeover/
    └── SKILL.md
```

- `README.md`: Chinese documentation.
- `README_EN.md`: English documentation.
- `project-takeover/SKILL.md`: Skill.
