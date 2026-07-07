# UHAKIKA Release Process

UHAKIKA AGENT releases are intentionally review-first. The release workflow publishes from an existing signed tag instead of creating one automatically in CI.

## Release Gate

- Main branch is clean and pushed.
- UHAKIKA CI passes.
- Build passes locally or in CI.
- Relevant tests pass or skipped checks are explained.
- Release notes describe what changed and any compatibility impact.
- Rollback path is known.

## Signed Tag Flow

```bash
git checkout main
git pull --ff-only origin main
bun install
bun run build
bun run test:free
git tag -s uhakika-v1.58.5.1 -m "UHAKIKA AGENT 1.58.5.1"
git push origin uhakika-v1.58.5.1
```

Then run the `UHAKIKA Release` workflow from GitHub Actions with:

```text
version = 1.58.5.1
```

The workflow verifies the signed tag before publishing the GitHub release.

## Unsigned Emergency Release

Avoid unsigned releases. If an emergency requires one, document:

- why signing was not possible
- who approved the exception
- what validation was completed
- how the next signed release will supersede it

