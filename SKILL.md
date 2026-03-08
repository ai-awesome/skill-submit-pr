---
name: submit-pr
---

# Submit PR Skill

1. Ensure you are on a feature branch (never main/master). If on main, create a new branch named `<type>/<short-description>` (e.g. `feat/add-login`, `fix/null-pointer`).
2. Before committing, run build and test commands. If tests fail, fix the issues and re-run until green.
3. Stage changes for commit. Exclude sensitive files (`.env`, credentials, secrets, private keys) and large binaries. When in doubt, ask the user before staging.
4. Commit with a message following Conventional Commits format: `<type>(<scope>): <description>` (e.g. `feat(auth): add OAuth2 login flow`). Keep the subject line under 72 characters.
5. Rebase onto the latest target branch to ensure no merge conflicts before pushing.
6. Push the branch to origin.
7. Create a PR with a description that accurately reflects the actual diff, not the planned changes.
8. Show the PR URL to the user.
9. After submitting the PR, proactively monitor the GitHub Actions workflow status. If any workflow fails, investigate the failure, fix the issue, push the fix, and re-check until all checks are green.

Never force-push to main/master.
