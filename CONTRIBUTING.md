# CONTRIBUTING.md

This holds guide to contribute to this repo.

## Branching Strategy

We use a clear branching model to keep devment organized and the main branch stable.

### Branch Structure

| Branch | Purpose |
|--------|---------|
| `main` | Stable, production-ready code. No direct commits allowed. |
| `dev` | Primary working branch. All features land here first. |
| `feature/<name>` | For new features. Always branch from `dev`. Example: `feature/user-profile` |
| `bugfix/<name>` | For fixing bugs in devment. Branch from `dev`. |
| `hotfix/<name>` | Urgent production fixes. Branch from `main` directly. |
| `release/<version>` | Pre-release staging. Example: `release/2.0.0` |

> [!note]
> You can also use shoter version of the words, like `feat`, `fix`, `dev`, `rel` etc.

### How It Works

1. Create your branch from `dev` — never from `main`.
2. Once your work is done, open a Pull Request targeting `dev`.
3. After review and approval, `dev` gets merged into `main` for release.
4. Hotfixes go directly from `main` and must be merged back into both `main` and `dev`.


## Collaborative Coding Guidelines

### Commit Message Format

Use this structure: `type(scope): description`

Common types:
- `feat` — a new feature
- `fix` — a bug fix
- `docs` — documentation changes
- `refactor` — code restructuring without behavior change
- `test` — adding or updating tests

Examples:
- `feat(auth): add password reset functionality`
- `fix(navbar): correct broken mobile menu toggle`
- `docs(readme): add local setup instructions`

### Branch Naming

- Lowercase only, use hyphens between words
- Pattern: `type/brief-description`
- Examples: `feature/chat-module`, `bugfix/session-timeout`, `hotfix/payment-crash`

### Before Pushing

- Code must run without errors locally
- Remove any debug logs or temporary code
- Never commit `.env` files or sensitive credentials
- Make sure existing functionality still works

### Resolving Merge Conflicts

1. Always sync with the target branch before starting: `git pull origin dev`
2. Resolve conflicts locally using your editor
3. Stage resolved files: `git add <filename>`
4. Complete the merge with: `git commit`
5. Never force-push to `main` or `dev`
6. When in doubt, discuss with the teammate whose code conflicts with yours

### Team Rules

- Pull Requests are mandatory — no direct pushes to `main` or `dev`
- Each PR must be reviewed and approved before merging
- Keep PRs small and focused on one thing
- Leave constructive review comments, not just approvals
- Communicate openly when you're blocked or unsure
