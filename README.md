# .github

Default community health files for all repositories under [@KevinDeBenedetti](https://github.com/KevinDeBenedetti).

## Overview

This is a special public repository. GitHub automatically uses its community health files as defaults for any repository owned by the account that does not define its own. If a repository has its own file (e.g. `CONTRIBUTING.md` or `.github/ISSUE_TEMPLATE/`), it takes precedence over the defaults here.

> Reusable workflows and composite actions live in a separate repository: [`github-workflows`](https://github.com/KevinDeBenedetti/github-workflows).

## Structure

```
.
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
├── SUPPORT.md
└── .github/
    ├── CODEOWNERS
    ├── FUNDING.yml
    ├── PULL_REQUEST_TEMPLATE.md
    ├── DISCUSSION_TEMPLATE/
    │   ├── announcements.yml
    │   ├── general.yml
    │   └── q-and-a.yml
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        ├── config.yml
        └── feature_request.md
```

## Contents

### Community Health Files

| File                 | Description                                                                      |
| -------------------- | -------------------------------------------------------------------------------- |
| `CODE_OF_CONDUCT.md` | Contributor Covenant v2.1 — expectations for community behavior                  |
| `CONTRIBUTING.md`    | How to report bugs, suggest features, and submit pull requests                   |
| `SECURITY.md`        | Supported versions, vulnerability reporting process, and security best practices |
| `SUPPORT.md`         | Where to get help (Discussions, issues, docs)                                    |

### Issue Templates

| Template            | Label         | Description                               |
| ------------------- | ------------- | ----------------------------------------- |
| `🐛 Bug report`      | `bug`         | Structured report for reproducing bugs    |
| `✨ Feature request` | `enhancement` | Proposal for new features or improvements |

Blank issues are disabled — contributors must use a template or open a [Discussion](https://github.com/KevinDeBenedetti/KevinDeBenedetti/discussions).

### Pull Request Template

Located at `.github/PULL_REQUEST_TEMPLATE.md`. Prompts contributors to describe their changes, classify the PR type (bug fix, feature, docs, refactor, CI, breaking change), and confirm a checklist before submitting.

### Discussion Templates

Located in `.github/DISCUSSION_TEMPLATE/`. Pre-fills new discussion forms by category.

| Template              | Label          | Description                                       |
| --------------------- | -------------- | ------------------------------------------------- |
| `📣 announcements.yml` | `announcement` | Official announcements from maintainers           |
| `💬 general.yml`       | —              | Open-ended conversations and feedback             |
| `❓ q-and-a.yml`       | `question`     | Structured Q&A with checklist to avoid duplicates |

### Code Owners

`.github/CODEOWNERS` assigns `@KevinDeBenedetti` as the default reviewer for all files in this repository.

### Funding

`.github/FUNDING.yml` links [GitHub Sponsors](https://github.com/sponsors/KevinDeBenedetti) to this account.

## References

- [GitHub Docs — Default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [GitHub Docs — About issue and pull request templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests)
- [GitHub Docs — About code owners](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

