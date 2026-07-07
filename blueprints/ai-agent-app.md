# AI Agent App

## Use Case
Application that uses one or more AI agents to reason, plan, act, or assist.

## Recommended Architecture
Separate orchestration, tool access, memory, safety policy, evaluation, and UI/API layers.

## Folder Structure
`agents/`, `tools/`, `memory/`, `evals/`, `policies/`, `src/`, `docs/`.

## Core Components
Agent loop, prompts, tool registry, permissions, memory, eval harness, audit logs.

## Required Decisions
Model choices, tool boundaries, human approval gates, memory scope, evaluation criteria.

## Security Notes
Defend against prompt injection, protect secrets, isolate tools, log risky decisions.

## Testing Strategy
Unit tests, tool contract tests, scenario evals, safety evals, regression suites.

## Deployment Notes
Document model config, secrets, permissions, rate limits, rollback, and monitoring.

## Common Failure Modes
Unbounded tool access, unclear success criteria, hidden prompt drift, missing evals.

## MVP Checklist
- [ ] Mission and safety policy defined
- [ ] Tool boundaries reviewed
- [ ] Evals created
- [ ] Human approval gates documented
- [ ] Handoff complete
