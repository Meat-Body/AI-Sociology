# Release Process

This repository uses staged public releases.

The goal is not to publish every idea as soon as it appears. The goal is to keep the public entry point clear, while letting deeper branches mature in candidate drafts, RFCs, human-readable GitHub drafts, and backlog documents.

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
- `v0.6-dao-of-fusion`
- `v0.7-silent-distribution-protocol`
- `v0.8-return-flow-and-first-principles`
- `v1.0-kernel-candidate`
- `v1.0-carbon-silicon-civilization-protocol`

## Final source version

`v1.0-carbon-silicon-civilization-protocol` is intended to be the formal initial version and the last source-repository version.

It should be tagged only after:

- `v1.0-kernel-candidate` has stabilized;
- limited calibration has been completed;
- real AI/Agent-mediated human return or concrete external misreadings have produced any necessary corrections, if available;
- de-identification boundaries have been checked;
- machine-readable summaries and protocol index are consistent.

After `v1.0`, the repository enters board lock.

Do not create further mainline version releases after `v1.0`.

Substantial future work should happen in forks or independent repositories.

This closes the source kernel, not the ecosystem.

## Before tagging a release

- Confirm the worktree is clean.
- Confirm README links point to the right public entry files.
- Confirm `PROTOCOL_INDEX.md` distinguishes released files from staging candidates.
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
- Put new expansions in candidate docs, RFCs, human-readable GitHub drafts, or `docs/09_protocol_growth_backlog.md`.
- If a released concept changes meaning, explain the change in `CHANGELOG.md` instead of silently rewriting the historical anchor.
