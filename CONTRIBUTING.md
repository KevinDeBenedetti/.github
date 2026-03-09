# Contributing

Thank you for considering a contribution! This document explains how to report bugs, suggest features, and submit pull requests.

## Table of Contents

- [Contributing](#contributing)
  - [Table of Contents](#table-of-contents)
  - [Code of Conduct](#code-of-conduct)
  - [Getting Started](#getting-started)
  - [How to Contribute](#how-to-contribute)
    - [Reporting Bugs](#reporting-bugs)
    - [Suggesting Features](#suggesting-features)
    - [Submitting a Pull Request](#submitting-a-pull-request)
  - [Style Guide](#style-guide)
  - [Commit Message Convention](#commit-message-convention)

---

## Code of Conduct

This project is governed by the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).
By participating you agree to abide by its terms.

---

## Getting Started

1. **Fork** the repository and clone your fork locally.
2. Create a dedicated **branch** for your change:
   ```bash
   git checkout -b feat/my-improvement
   ```
3. Make your changes, following the [style guide](#style-guide) below.
4. **Test** your changes before opening a pull request.
5. Push your branch and open a **pull request** against `main`.

---

## How to Contribute

### Reporting Bugs

- Search [existing issues](../../issues) first to avoid duplicates.
- Use the **🐛 Bug report** template when opening a new issue.
- Include clear reproduction steps, the expected vs. actual behavior, and your environment.
- Never include secrets, credentials, or personal data in an issue.

### Suggesting Features

- Search [existing issues](../../issues) and [discussions](../../discussions) first.
- Use the **✨ Feature request** template when opening a new issue.
- Describe the problem your idea solves and the proposed solution.

### Submitting a Pull Request

1. Keep changes **focused** — one concern per pull request.
2. Reference the related issue(s) in the PR description (`Closes #123`).
3. Fill in the [pull request template](.github/PULL_REQUEST_TEMPLATE.md) completely.
4. Ensure all CI checks pass before requesting review.
5. Be responsive to review feedback — address comments within a reasonable time.

---

## Style Guide

- **YAML** files: 2-space indentation, explicit string quoting where ambiguous.
- **Markdown**: ATX headings (`#`), blank line between sections, 80-char soft wrap.
- **Workflow files**: one step per action, pinned action SHA for third-party actions.
- Keep names, labels, and descriptions in **English**.

---

## Commit Message Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(scope): <short description>

[optional body]

[optional footer]
```

| Type       | When to use                                |
| ---------- | ------------------------------------------ |
| `feat`     | A new feature or template                  |
| `fix`      | A bug fix                                  |
| `docs`     | Documentation only                         |
| `chore`    | Maintenance tasks (deps, config)           |
| `refactor` | Code restructuring without behavior change |
| `ci`       | CI/CD workflow changes                     |

Examples:

```
feat(issue-template): add question template
fix(workflows): correct pnpm cache key
docs: update CONTRIBUTING guide
```

---

Questions? Open a [Discussion](https://github.com/KevinDeBenedetti/KevinDeBenedetti/discussions) instead of an issue.
