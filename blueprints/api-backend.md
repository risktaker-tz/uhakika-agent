# API Backend

## Use Case
Service that exposes programmatic capabilities to clients or other services.

## Recommended Architecture
Use layered request handling, validation, domain logic, persistence, and observability.

## Folder Structure
`src/routes/`, `src/services/`, `src/data/`, `src/middleware/`, `tests/`, `docs/`.

## Core Components
Routing, validation, auth, business logic, storage access, error handling, telemetry.

## Required Decisions
Protocol, schema strategy, auth model, data storage, rate limits, versioning.

## Security Notes
Validate every boundary, protect secrets, rate-limit abuse paths, review permissions.

## Testing Strategy
Unit tests, integration tests, contract tests, negative tests, load smoke checks.

## Deployment Notes
Document environment variables, migrations, health endpoints, rollback steps.

## Common Failure Modes
Unclear contracts, silent auth bypass, inconsistent errors, missing migration plan.

## MVP Checklist
- [ ] API contract documented
- [ ] Auth and validation reviewed
- [ ] Tests cover success and failure paths
- [ ] Observability in place
- [ ] Rollback path documented
