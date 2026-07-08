# Fells Code Repository Standards

This document is the maintenance bar for every repository in the `fells-code`
organization. It exists so the ecosystem stays consistent, inspectable, and
trustworthy for adopters and contributors. Repositories may extend these
standards but must not contradict them.

## Required Files

Every repository should have:

- `README.md` that describes what the project is and how to use it (not a
  framework starter template).
- `AGENTS.md` containing the shared "Working Standards (fells-code baseline)"
  block plus repo-specific guidance.
- `LICENSE` appropriate to the project (see Licensing).

The following are provided organization-wide by the `fells-code/.github`
repository and apply automatically to any repo that does not define its own:

- `CODE_OF_CONDUCT.md`
- `CONTRIBUTING.md`
- `SECURITY.md`
- Issue templates and a pull request template

## Toolchain Baseline (Node projects)

- Node 24 (current LTS) is the standard. Pin it with a `.nvmrc` containing `24`.
- Declare `engines.node` as `>=24 <25` (keep any existing `npm`/`pnpm`
  constraints).
- `.nvmrc` is the single source of truth. CI reads it with `setup-node`'s
  `node-version-file: .nvmrc` rather than a hardcoded version. Exception:
  reusable cross-repo workflows that check out sibling repos pin the version
  directly, since there is no single `.nvmrc` in that context.
- Containerized services also pin the Node major in their `Dockerfile` base
  image; that is the deployed runtime, not `.nvmrc`.

## AGENTS.md Baseline

Every repository's `AGENTS.md` includes a `## Working Standards (fells-code
baseline)` section covering:

- **Attribution**: commit and open PRs under the repository owner's identity;
  never add AI or assistant attribution anywhere.
- **Comments**: only where the code genuinely needs explaining; never narrate
  what the code plainly does.
- **TODOs**: every `TODO`/`FIXME` references a tracking issue.
- **Commits and branches**: Conventional Commits; descriptive, type-prefixed
  branch names; never a tool-generated prefix.
- **Public-facing text**: no em dashes in commits, comments, PR or issue text,
  changesets, or docs.
- **Before declaring work done**: all applicable checks (tests, lint, type
  check, formatting) must pass before opening a PR.

## Branching and Releases

- `main` is the source of truth for every repository. Long-lived `dev` branches
  are being retired to prevent drift.
- Repositories that publish packages use Changesets; do not hand-edit versions
  or changelogs.

## Verification

Do not claim a change works without running the relevant checks and reporting
real output. Typical checks are `typecheck`, `lint`, `format:check` (or the
Terraform, Rust, or shell equivalents), and the test suite. Containerized and
integration paths may require services that only run in CI; say so explicitly
when a check cannot be run locally.

## Licensing

- **Open-source components** (the public Seamless Auth stack that adopters
  self-host: the API, server adapters, SDKs, shared types, CLI, messaging,
  starters, templates, docs, and Seamless Secrets) are licensed under
  **AGPL-3.0-only**.
- **Product, hosted, and internal components** (Glance and its site/distribution,
  the hosted Portal and its API, the Review product, internal APIs, and
  infrastructure repositories) are **proprietary**: source may be visible, but
  they are not open-source licensed.

Each repository states its own license in a `LICENSE` file so the terms are
unambiguous.
