# Host Aliases

UHAKIKA AGENT preserves upstream `gstack` internal names where they are part of binary names, generated host artifacts, state directories, or compatibility contracts.

## Current Rule

Use UHAKIKA AGENT in user-facing documentation and project positioning. Preserve legacy internal names where changing them would break setup, generated skills, existing scripts, or future upstream sync.

## Alias Strategy

Phase 3 supports a gradual alias strategy:

- keep upstream-compatible internals stable
- expose UHAKIKA terminology in README and docs
- add optional wrappers only after tests cover setup, install, and host behavior
- avoid hiding upstream attribution or MIT license history

## Candidate Future Aliases

Potential aliases should be added only after validation:

- `uhakika-agent` as a top-level command wrapper
- `uhakika` as a short command wrapper
- UHAKIKA-prefixed generated host skill names where the host allows aliases

Any alias must call the existing tested implementation rather than duplicate logic.

