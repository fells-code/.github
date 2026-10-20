# Governance

How the projects in the `fells-code` organization are run: who decides, how releases
happen, how security reports are handled, and what the Seamless Auth license will and
will not do. A repository may add to this in its own `GOVERNANCE.md`, but not contradict it.

## Maintainers

The projects are maintained by Fells Code, LLC. Today that is one person,
Brandon Corbett ([@Bccorb](https://github.com/Bccorb)), who reviews and merges every
change, cuts every release and handles every security report.

One maintainer is a real limit, and it is stated here rather than left for you to find:
response times are targets, not guarantees, and there is no second person who can cut a
release today. When that changes, this document will name the new maintainers.

## How Decisions Are Made

- **In the open.** Plans, bugs and design questions are GitHub issues. Larger work is
  tracked as an epic issue with child issues, so the reasoning for a change can be read
  later. Security work in progress is the exception (see below).
- **By the maintainer.** Anyone can propose a change in an issue or a pull request. The
  maintainer decides, and says why when declining.
- **Recorded.** A decision that changes a public contract (an HTTP route, a token claim, a
  package API) is written down in the pull request that makes it, and in the changeset
  that ships it.

## Releases

- Every repository versions and publishes with [Changesets](https://github.com/changesets/changesets).
  A merged change that users will notice carries a changeset, the changesets collect into a
  release pull request, and merging that pull request is the release. The maintainer approves
  and merges every release pull request.
- npm packages are published from CI, not from a developer machine.
- The Seamless Auth API container image is built in CI, signed with cosign keyless signing,
  and published with an SBOM and a provenance attestation. How to verify it is in that
  repository's `SECURITY.md`.
- The Seamless Auth packages are pre-1.0. Under 0.x a minor release may contain a breaking
  change, which its changelog entry describes. Version 1.0 will be a deliberate decision,
  not the side effect of a change.

## Security Reports

Report vulnerabilities privately, as described in [SECURITY.md](SECURITY.md) or the
repository's own `SECURITY.md`, never in a public issue. A confirmed vulnerability is fixed
and released before it is disclosed, then published as a GitHub security advisory that names
the affected and patched versions. Security fixes go to the latest release line; there are no
backports to older minor versions.

## The Seamless Auth License Pledge

Seamless Auth is Apache-2.0, and it stays that way:

- **No enterprise edition.** There is no paid or closed version of the software, and there
  will not be one.
- **Features stay open.** Single sign-on, SCIM, multi-factor authentication, organizations,
  and security features such as audit logging and admin controls are part of the open source
  product, and will stay in it.
- **No relicensing.** Code released under Apache-2.0 will not be moved to a source-available
  or more restrictive license.
- **What is sold is hosting and support.** Any managed Seamless Auth offering charges for
  running the software and for support, never for features that are missing from the open
  source release.

This pledge applies to every Seamless Auth repository in this organization: the API, the
server adapters, the client SDKs, the CLI, the admin dashboard and the shared packages.

## Changing This Document

Changes to this document are made by pull request to
[`fells-code/.github`](https://github.com/fells-code/.github), so its history is public.
