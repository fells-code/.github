# Contributing to Fells Code projects

Thanks for contributing. This guide applies to every repository in the
`fells-code` organization unless a repository provides its own
`CONTRIBUTING.md`. Individual repositories may add repo-specific setup and
guidance on top of it.

Read the repository's `AGENTS.md` first. It describes the architecture, the
conventions the repository enforces, and the checks to run before opening a PR.
The organization-wide standards live in [REPO-STANDARDS.md](REPO-STANDARDS.md).

## Before You Start

For non-trivial changes, open an issue first, explain the motivation and your
proposed approach, and wait for feedback. Small fixes and docs improvements can
go straight to a pull request.

## Working Standards

These apply across the organization:

- **Node version**: repositories with a Node toolchain pin Node 24 via `.nvmrc`
  and `engines`. Run `nvm use` before installing.
- **Commits**: follow [Conventional Commits](https://www.conventionalcommits.org)
  (`feat:`, `fix:`, `chore:`, `docs:`, `ci:`, `test:`). Many repositories enforce
  this with commitlint on a commit hook.
- **Branches**: use a descriptive, type-prefixed name (`feat/...`, `fix/...`,
  `chore/...`). Do not use tool-generated branch prefixes.
- **Attribution**: commit and open PRs under your own identity. Do not add AI or
  assistant attribution (no `Co-Authored-By` trailers for assistants, no
  "Generated with" notes) anywhere in commits, PRs, issues, changesets, or docs.
- **Comments**: comment only where the code genuinely needs explaining. Do not
  narrate what the code plainly does.
- **TODOs**: every `TODO`/`FIXME` must reference a tracking issue.
- **Public-facing text**: no em dashes in commits, comments, PR or issue text,
  changesets, or docs. Use a comma, parentheses, or a separate sentence.

## Before You Open a Pull Request

All code quality checks that apply to the repository must pass: tests, linting,
type checks, and formatting. Run them and confirm the real output. Do not open a
PR while a relevant check is failing.

Keep pull requests focused and describe the change and its motivation. Link the
issue it addresses.

## Code of Conduct

Participation is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). Report
concerns to conduct@fells.codes.

## Security

Do not report security issues in public issues or pull requests. Follow the
[Security Policy](SECURITY.md).
