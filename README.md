# .github

[![CI/CD](https://img.shields.io/github/actions/workflow/status/KevinDeBenedetti/.github/ci.yml?style=for-the-badge&label=CI%2FCD)](https://github.com/KevinDeBenedetti/.github/actions/workflows/ci.yml)

> Default community health files for every repository of [@KevinDeBenedetti](https://github.com/KevinDeBenedetti) that does not define its own.

## Features

- `CODE_OF_CONDUCT.md` — Contributor Covenant 3.0, with a private reporting channel
- `CONTRIBUTING.md` — how to report bugs, suggest features, and submit pull requests, and the commit types
- `SECURITY.md` — private vulnerability reporting, supported versions, and scope
- `SUPPORT.md` — where to find the docs, ask a question, or report a bug
- Issue templates (🐛 Bug report, ✨ Feature request; blank issues disabled) and a pull request template whose summary the [pr-description workflow](https://kevindebenedetti.github.io/github-workflows/workflows/pr-description) writes from the commits, where it runs
- Discussion templates (announcements, general, Q&A) for repositories that enable Discussions

## Usage

GitHub uses each of these files in every repository of the account, public or private, that has no file of the same type in its `.github/` folder, its root, or its `docs/` folder. A repository's own file always takes precedence:

```text
my-repo/
└── .github/
    └── SECURITY.md   # replaces the default SECURITY.md in my-repo only
```

A repository with its own `.github/ISSUE_TEMPLATE/` folder gets none of the default issue templates. `CODEOWNERS`, `prek.toml`, and the CI workflow apply to this repository only.

> Reusable workflows and composite actions live in a separate repository: [`github-workflows`](https://github.com/KevinDeBenedetti/github-workflows).

## Git hooks

The [prek](https://prek.j178.dev) hooks of `prek.toml` check file hygiene, YAML, and the workflows; CI runs them on every push and pull request.

```sh
prek install           # once after cloning
prek run --all-files
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

To report a vulnerability, see [SECURITY.md](SECURITY.md).
