# Mobile App

## Use Case
Mobile-first application with native or cross-platform delivery.

## Recommended Architecture
Separate UI, state, service clients, storage, platform integrations, and release config.

## Folder Structure
`app/`, `features/`, `services/`, `components/`, `tests/`, `docs/`.

## Core Components
Screens, navigation, local state, remote calls, offline behavior, permissions.

## Required Decisions
Platform, framework, navigation, offline needs, release process, testing devices.

## Security Notes
Minimize stored secrets, validate server-side, review permissions and local storage.

## Testing Strategy
Unit, integration, device smoke, accessibility, release candidate checks.

## Deployment Notes
Document signing, build profiles, environment config, release channels, rollback.

## Common Failure Modes
Device-specific bugs, weak offline handling, permission surprises, release config drift.

## MVP Checklist
- [ ] Supported platforms defined
- [ ] Core flows validated on target devices
- [ ] Permissions reviewed
- [ ] Release path documented
- [ ] Handoff complete
