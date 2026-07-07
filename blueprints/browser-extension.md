# Browser Extension

## Use Case
Extension that augments browser workflows with UI, automation, or integration logic.

## Recommended Architecture
Separate background logic, content scripts, UI surfaces, permissions, messaging, and storage.

## Folder Structure
`extension/`, `src/background/`, `src/content/`, `src/ui/`, `tests/`, `docs/`.

## Core Components
Manifest, background worker, content scripts, UI, message bridge, storage, permissions.

## Required Decisions
Manifest version, permissions, target pages, data handling, packaging, release process.

## Security Notes
Use least privilege, validate messages, avoid leaking page data, review injection surfaces.

## Testing Strategy
Unit, browser integration, permission checks, install/update smoke tests.

## Deployment Notes
Document packaging, signing, store submission, versioning, rollback.

## Common Failure Modes
Overbroad permissions, message spoofing, brittle selectors, update breakage.

## MVP Checklist
- [ ] Permissions justified
- [ ] Messaging validated
- [ ] Browser smoke tests pass
- [ ] Release process documented
- [ ] Handoff complete
