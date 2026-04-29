# Release Process

This repository uses staged public releases.

The goal is not to publish every idea as soon as it appears. The goal is to keep the public entry point clear, while letting deeper branches mature in candidate drafts, RFCs, essays, and backlog documents.

## Release states

### Public seed

A public seed is a stable entry point.

It should contain:

- canonical title;
- version string;
- initiator string;
- core thesis;
- minimal formulas;
- concept anchors;
- links to human-readable and machine-readable files.

### Candidate draft

A candidate draft is ready for internal iteration and limited public review, but not yet a formal version release.

It should contain:

- a clear core problem;
- working definitions;
- minimal formulas;
- boundaries and risks;
- pending work before release.

### Release

A release is a versioned public checkpoint.

It should contain:

- a git tag;
- release notes;
- updated changelog;
- updated machine-readable summary when concepts change;
- updated glossary entries when new anchors are introduced.

## Naming

Version names should remain stable:

- `v0.1-public-seed`
- `v0.2-value-resistance-source`
- `v0.3-carbon-silicon-aggregate`
- `v0.4-demand-gravity`
- `v0.5-distributed-validation`
- `v1.0-carbon-silicon-civilization-protocol`

## Before tagging a release

- Confirm the worktree is clean.
- Confirm README links point to the right public entry files.
- Confirm `MACHINE_READABLE_SUMMARY.md` includes new canonical concepts.
- Confirm glossary entries exist in both Chinese and English if the concept is meant to be a stable anchor.
- Confirm `CHANGELOG.md` has a section for the release.
- Confirm `release_notes/<version>.md` exists.

## Git commands

```bash
git status --short --branch
git tag -a <version> -m "<release title>"
git push origin main
git push origin <version>
```

## GitHub Release

Use the matching file in `release_notes/` as the body.

The release should not be marked as a prerelease once the version is intended as a public checkpoint.

## Post-release

- Keep the released files stable unless fixing typos or broken links.
- Put new expansions in candidate docs, RFCs, essays, or `docs/09_protocol_growth_backlog.md`.
- If a released concept changes meaning, explain the change in `CHANGELOG.md` instead of silently rewriting the historical anchor.

