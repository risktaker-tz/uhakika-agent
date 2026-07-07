# Monorepo

## Use Case
Repository that contains multiple apps, packages, services, or shared tooling.

## Recommended Architecture
Use clear ownership boundaries, shared tooling, dependency rules, and workspace validation.

## Folder Structure
`apps/`, `packages/`, `services/`, `tools/`, `docs/`, `tests/`.

## Core Components
Workspace config, package boundaries, build graph, test graph, release process.

## Required Decisions
Package manager, build tool, versioning, ownership, dependency policy, CI strategy.

## Security Notes
Protect shared scripts, review dependency graph, avoid secrets in shared config.

## Testing Strategy
Affected tests, full regression gates, package contract tests, build verification.

## Deployment Notes
Document release ownership, versioning, CI gates, rollback per component.

## Common Failure Modes
Unclear ownership, accidental cross-dependencies, slow CI, brittle shared scripts.

## MVP Checklist
- [ ] Workspace boundaries documented
- [ ] Build/test commands defined
- [ ] Dependency rules reviewed
- [ ] CI strategy documented
- [ ] Handoff complete
