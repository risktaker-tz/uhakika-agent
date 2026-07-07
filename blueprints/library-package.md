# Library Package

## Use Case
Reusable package consumed by applications, services, or other packages.

## Recommended Architecture
Keep public API stable, internals modular, tests comprehensive, and docs close to usage.

## Folder Structure
`src/`, `test/`, `docs/`, `examples/`, `scripts/`.

## Core Components
Public API, internal modules, types, tests, examples, release metadata.

## Required Decisions
Runtime support, module format, API surface, versioning, compatibility policy.

## Security Notes
Avoid unsafe defaults, validate inputs, review dependency exposure, protect release keys.

## Testing Strategy
Unit, API contract, compatibility, example, package install checks.

## Deployment Notes
Document build, publish, versioning, changelog, rollback or deprecation process.

## Common Failure Modes
Breaking API changes, weak examples, missing type coverage, publish config mistakes.

## MVP Checklist
- [ ] Public API documented
- [ ] Package install tested
- [ ] Versioning policy clear
- [ ] Examples verified
- [ ] Release notes prepared
