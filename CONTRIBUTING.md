# Contributing

Thank you for considering a contribution! This guide applies to every
repository of [@KevinDeBenedetti](https://github.com/KevinDeBenedetti) that
has no `CONTRIBUTING.md` of its own.

## Code of Conduct

This project is governed by the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).
By participating you agree to abide by its terms.

## Reporting bugs and suggesting features

- Search the existing issues of the repository first, to avoid duplicates.
- Use the **🐛 Bug report** template for a bug: clear reproduction steps, the
  expected vs. actual behavior, and your environment.
- Use the **✨ Feature request** template for an idea: the problem it solves
  and the solution you propose.
- Never include secrets, credentials, or personal data in an issue. Report
  security vulnerabilities privately, as described in [SECURITY.md](SECURITY.md).
- For questions, see [SUPPORT.md](SUPPORT.md).

## Submitting a pull request

1. **Fork** the repository and create a dedicated **branch** from `main`:
   ```bash
   git checkout -b feat/my-improvement
   ```
2. When the repository has a `prek.toml`, install its git hooks once with
   `prek install` ([prek](https://prek.j178.dev)).
3. Keep changes **focused** — one concern per pull request — and test them.
4. Fill in the [pull request template](.github/PULL_REQUEST_TEMPLATE.md) and
   reference the related issue(s) (`Closes #123`). Where the pr-description
   workflow runs, Summary and Changes are written from the commits: complete
   the other sections.
5. Ensure all CI checks pass, then address review comments within a
   reasonable time.

## Style guide

- **YAML** files: 2-space indentation, explicit string quoting where ambiguous.
- **Markdown**: ATX headings (`#`), blank line between sections, 80-char soft wrap.
- **GitHub Actions**: pin actions and reusable workflows to a full commit SHA
  with a version comment (`@<sha> # v1.2.3`), never to a branch.
- Keep names, labels, comments, and documentation in **English**.

## Commit message convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
Where a repository publishes releases, release-please builds the version and
the changelog from them.

```
<type>(<scope>)<!>: <summary>

[optional body]

[optional footer]
```

| Type     | When to use                                           | Changelog section        |
| -------- | ----------------------------------------------------- | ------------------------ |
| `feat`   | A new feature                                         | Features                 |
| `fix`    | A bug fix                                             | Bug Fixes                |
| `perf`   | A performance improvement                             | Performance Improvements |
| `revert` | Reverting an earlier commit                           | Reverts                  |
| `deps`   | Dependency updates                                    | hidden                   |
| `docs`   | Documentation only                                    | hidden                   |
| `style`  | Formatting, no change in behavior                     | hidden                   |
| `test`   | Tests only                                            | hidden                   |
| `build`  | Build system or packaging                             | hidden                   |
| `ci`     | CI/CD workflow changes                                | hidden                   |
| `chore`  | Maintenance, or a refactor with no visible effect     | hidden                   |

- Do not use `refactor`: a pure refactor is a `chore`.
- Write the summary in the imperative, starting lowercase, with no trailing
  period; keep the whole header within 100 characters.
- Mark a breaking change with `!` before the colon (`feat(api)!: …`).

Examples:

```
feat(issue-template): add question template
fix(workflows): correct pnpm cache key
docs: update CONTRIBUTING guide
```
