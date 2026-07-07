# Fullstack App

## Use Case
General application with client, server, persistence, and deployment surfaces.

## Recommended Architecture
Separate presentation, application logic, data access, and infrastructure concerns.

## Folder Structure
`apps/`, `packages/`, `server/`, `docs/`, `tests/`.

## Core Components
Client UI, API layer, persistence layer, authentication boundary, validation, observability.

## Required Decisions
Runtime, framework, data model, auth model, deployment target, validation strategy.

## Security Notes
Protect secrets, validate inputs, enforce authorization, log safely, review dependency risk.

## Testing Strategy
Unit, integration, contract, browser, accessibility, and release smoke checks.

## Deployment Notes
Define environments, configuration, migrations, rollback, health checks, and monitoring.

## Common Failure Modes
Leaky boundaries, untested integration paths, fragile configuration, weak authorization.

## MVP Checklist
- [ ] Mission and users defined
- [ ] Architecture boundaries documented
- [ ] Core flows tested
- [ ] Security review completed
- [ ] Rollback path documented
