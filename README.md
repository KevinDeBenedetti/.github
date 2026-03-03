# .github

Default community health files and reusable workflows for all repositories under [@KevinDeBenedetti](https://github.com/KevinDeBenedetti).

## Overview

This repository provides shared GitHub configuration applied automatically across all public repositories that do not define their own equivalents.

## Contents

### Issue Templates

| Template            | Description                                            |
| ------------------- | ------------------------------------------------------ |
| `🐛 Bug report`      | Structured report for identifying and reproducing bugs |
| `✨ Feature request` | Proposal for new features or improvements              |

Blank issues are disabled — all contributors use a template or open a [Discussion](https://github.com/KevinDeBenedetti/KevinDeBenedetti/discussions).

### Pull Request Template

Located at `.github/PULL_REQUEST_TEMPLATE.md`. Prompts contributors to describe their changes, classify the type of change, and confirm their checklist before opening a PR.

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
      codeql-languages: javascript,typescript  # default
```

> **Note:** The `audit-node` and `audit-python` jobs rely on composite actions `actions/setup-node` and `actions/setup-python` located in this repository.

## References

- [GitHub Docs — Default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [GitHub Docs — Reusing workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows)

