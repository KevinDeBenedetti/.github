# Security Policy

## Supported Versions

Community health files and reusable workflows in this repository are actively maintained.
Only the latest version on the `main` branch is supported.

| Version | Supported |
| ------- | --------- |
| `main`  | ✅         |

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability, use one of the following private channels:

1. **GitHub Private Security Advisory** — open a [Security Advisory](../../security/advisories/new) directly in this repository *(preferred)*.
2. **Email** — send details to the repository owner via the contact information on their [GitHub profile](https://github.com/KevinDeBenedetti).

### What to include

Please provide as much of the following as possible:

- A description of the vulnerability and its potential impact
- The affected file(s) or workflow(s)
- Steps to reproduce or a proof-of-concept
- Any suggested mitigation or fix

---

## Response Process

| Step                         | Target time              |
| ---------------------------- | ------------------------ |
| Acknowledgement of report    | 48 hours                 |
| Initial assessment           | 5 business days          |
| Fix & coordinated disclosure | Negotiated with reporter |

---

## Security Best Practices for Consumers

When calling reusable workflows from this repository:

- **Pin to a commit SHA** rather than a branch or floating tag to prevent supply-chain attacks.
- **Review workflow code** before using it in a sensitive pipeline.
- **Use least-privilege tokens** — pass only the permissions your workflow actually needs via `secrets`.
- **Audit third-party actions** used inside these workflows before granting them access to your secrets.

```yaml
# Recommended: pin to SHA
jobs:
  security:
    uses: KevinDeBenedetti/.github/.github/workflows/security.yml@<commit-sha>
```

---

## Scope

This policy covers the workflows, templates, and community health files hosted in this repository.
For vulnerabilities in projects that *consume* these workflows, please report to the respective repository.
