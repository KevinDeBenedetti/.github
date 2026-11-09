# Security policy

This is the default security policy of the repositories of
[@KevinDeBenedetti](https://github.com/KevinDeBenedetti): a repository with a
`SECURITY.md` of its own follows that one instead.

## Reporting a vulnerability

Please **do not open a public issue**. Report privately through GitHub:
**Security → Report a vulnerability** on the repository concerned (private
vulnerability reporting). If the repository does not offer that button, write
through the [contact form on kevindb.dev](https://kevindb.dev/en#contact)
instead.

Include the affected repository and file, the version (release tag or commit
SHA) and, if possible, a reproduction.

You can expect an acknowledgement within a few days. Fixes ship in the next
release; the advisory is published once that release is out.

## Supported versions

Only the latest release receives fixes. For a repository that does not
publish releases, that is the latest commit of its default branch.

## Scope

In scope: the code of the repository, what it publishes (packages, container
images, sites) and its GitHub Actions workflows. A vulnerability in a
third-party dependency belongs upstream; report it here as well when the way
the project uses that dependency makes it exploitable.
