# Automation System

## Use Case
System that performs repeatable tasks with minimal manual intervention.

## Recommended Architecture
Use explicit triggers, idempotent workers, queues where needed, logs, and rollback paths.

## Folder Structure
`src/triggers/`, `src/workers/`, `src/jobs/`, `src/lib/`, `tests/`, `docs/`.

## Core Components
Trigger, scheduler, worker, state store, retry policy, audit trail, alerting.

## Required Decisions
Trigger conditions, retry limits, failure handling, approval gates, observability.

## Security Notes
Limit permissions, protect credentials, avoid irreversible actions without approval.

## Testing Strategy
Unit, integration, dry-run, idempotency, failure and retry tests.

## Deployment Notes
Document schedules, secrets, job ownership, runbooks, rollback, and alert routing.

## Common Failure Modes
Duplicate execution, silent failure, runaway retries, broad permissions.

## MVP Checklist
- [ ] Dry-run mode defined
- [ ] Idempotency reviewed
- [ ] Failure handling tested
- [ ] Alerts configured
- [ ] Rollback documented
