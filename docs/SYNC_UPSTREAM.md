# Sync Upstream

UHAKIKA AGENT preserves the upstream update path from the original gstack project. The upstream default branch was detected as `main`.

Use a sync branch for every upstream update:

```bash
git fetch upstream
git checkout main
git checkout -b sync/upstream-$(date +%Y%m%d)
git merge upstream/main
```

Safe sync process:

1. Fetch upstream changes.
2. Create a sync branch.
3. Merge upstream into the sync branch.
4. Review conflicts carefully.
5. Preserve UHAKIKA AGENT branding.
6. Preserve custom skills and docs.
7. Run setup, build, and test validation.
8. Open a pull request into `main`.
9. Merge only after review.

Compatibility note: some internal command names, generated paths, and state directories still use the legacy `gstack` identifier. Preserve these during sync unless a dedicated compatibility migration updates scripts, tests, generated skill output, and host adapters together.
