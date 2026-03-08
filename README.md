# Submit PR Skill for Claude Code

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that automates the pull request submission workflow -- branching, building, testing, committing, pushing, PR creation, and CI monitoring -- in a single `/submit-pr` command. Requires the Claude Code CLI, git, and gh (GitHub CLI).

## What's Included

- **SKILL.md** -- The skill definition that drives the `/submit-pr` command. It ensures you are on a feature branch (creating one if on main/master), runs build and tests (fixing failures automatically), stages and commits changes, pushes to origin, creates a PR with a diff-based description, shows the PR URL, and monitors CI until green. The skill never force-pushes to main or master.

## Installation

Clone this repository:

```sh
git clone https://github.com/ai-awesome/skill-submit-pr.git
```

Then install the skill from the local path:

```sh
claude mcp add-skill /path/to/skill-submit-pr
```

Or install directly from the remote URL:

```sh
claude mcp add-skill https://github.com/ai-awesome/skill-submit-pr
```

## Customization

The skill is defined entirely in SKILL.md. Edit it to fit your workflow -- adjust the branching strategy, change the build/test commands, or modify the PR description format.

## Contributing

1. Fork this repository and create a feature branch.
2. Make your changes and ensure they are consistent with the existing style.
3. Submit a pull request with a clear description of what you changed and why.
