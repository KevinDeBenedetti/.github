# .github

Default community health files and reusable workflows for all repositories under [@KevinDeBenedetti](https://github.com/KevinDeBenedetti).

## Overview

This repository provides shared GitHub configuration applied automatically across all public repositories that do not define their own equivalents.

## Contents

### Community Health Files

| File                 | Description                                                                      |
| -------------------- | -------------------------------------------------------------------------------- |
| `CODE_OF_CONDUCT.md` | Contributor Covenant v2.1 — expectations for community behavior                  |
| `CONTRIBUTING.md`    | How to report bugs, suggest features, and submit pull requests                   |
| `SECURITY.md`        | Supported versions, vulnerability reporting process, and security best practices |
| `SUPPORT.md`         | Where to get help (Discussions, issues, docs)                                    |

### Issue Templates

| Template            | Description                                            |
| ------------------- | ------------------------------------------------------ |
| `🐛 Bug report`      | Structured report for identifying and reproducing bugs |
| `✨ Feature request` | Proposal for new features or improvements              |

Blank issues are disabled — all contributors use a template or open a [Discussion](https://github.com/KevinDeBenedetti/KevinDeBenedetti/discussions).

### Pull Request Template

Located at `.github/PULL_REQUEST_TEMPLATE.md`. Prompts contributors to describe their changes, classify the PR type, and confirm their checklist before opening a PR.

### Discussion Templates

Located in `.github/DISCUSSION_TEMPLATE/`. Pre-fills new discussion forms by category.

| Template            | Description                                       |
| ------------------- | ------------------------------------------------- |
| `announcements.yml` | Official announcements from maintainers           |
| `general.yml`       | Open-ended conversations and feedback             |
| `q-and-a.yml`       | Structured Q&A with checklist to avoid duplicates |

### Code Owners

`.github/CODEOWNERS` assigns automatic review requests to `@KevinDeBenedetti` for all files in this repository.

### Funding

`.github/FUNDING.yml` links GitHub Sponsors to this account.

### Reusable Workflows

All workflows are triggered via `workflow_call` and can be called from any repository.

| Workflow            | Description                                                                                                                           |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `security.yml`      | **Security audit** — dependency audit (pnpm / pip-audit), secret scanning (GitLeaks), and CodeQL SAST. Fully configurable via inputs. |
| `ci-node.yml`       | **CI for Node.js** — install, lint, build, and test a Node.js / pnpm project                                                          |
| `ci-python.yml`     | **CI for Python** — install (uv), lint, and test a Python project                                                                     |
| `release.yml`       | **Release** — automates releases via release-please                                                                                   |
| `deploy-docker.yml` | **Docker** — build and push an image to a container registry                                                                          |
| `deploy-pages.yml`  | **GitHub Pages** — build and deploy a static site                                                                                     |
| `deploy-vercel.yml` | **Vercel** — deploy to a preview or production environment                                                                            |

#### Usage example — security

```yaml
jobs:
  security:
    uses: KevinDeBenedetti/.github/.github/workflows/security.yml@main
    with:
      run-node-audit: true          # default: true
      run-python-audit: false       # default: false
      run-codeql: true              # default: true
      codeql-languages: '["javascript","typescript"]'  # JSON array
```

> **Note:** The `audit-node` and `audit-python` jobs rely on composite actions `actions/setup-node` and `actions/setup-python` located in this repository.

## References

- [GitHub Docs — Default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [GitHub Docs — Reusing workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows)

