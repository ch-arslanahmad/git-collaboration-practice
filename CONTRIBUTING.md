# CONTRIBUTING.md

This holds guide to contribute to this repo.

## Branching Strategy

We use a clear branching model to keep development organized and the main branch stable.

### Branch Structure

| Branch | Purpose |
|--------|---------|
| `main` | Stable, production-ready code. No direct commits allowed. |
| `develop` | Primary working branch. All features land here first. |
| `feature/<name>` | For new features. Always branch from `develop`. Example: `feature/user-profile` |
| `bugfix/<name>` | For fixing bugs in development. Branch from `develop`. |
| `hotfix/<name>` | Urgent production fixes. Branch from `main` directly. |
| `release/<version>` | Pre-release staging. Example: `release/2.0.0` |

> [!note]
> You can also use shoter version of the words, like `feat`, `fix`, `dev`, `rel` etc.

### How It Works

1. Create your branch from `develop` — never from `main`.
2. Once your work is done, open a Pull Request targeting `develop`.
3. After review and approval, `develop` gets merged into `main` for release.
4. Hotfixes go directly from `main` and must be merged back into both `main` and `develop`.
