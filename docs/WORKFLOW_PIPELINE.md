# Workflow Pipeline

Default UHAKIKA workflow:

```text
Clarify -> Plan -> Architect -> Build -> Review -> Test -> Secure -> Ship -> Document -> Handoff
```

| Stage | Purpose | Input | Output | Acceptance Criteria | Stop For Human Approval |
|---|---|---|---|---|---|
| Clarify | Remove ambiguity and define the mission. | Request, context, constraints. | Mission brief, questions, assumptions. | Goal, non-goals, constraints, and success criteria are clear. | When requirements conflict, scope is unclear, or risky assumptions are required. |
| Plan | Convert mission into ordered work. | Mission brief. | Milestones, tasks, validation plan. | Work is sequenced and validation is defined. | When tradeoffs affect scope, schedule, cost, or risk. |
| Architect | Decide structure before implementation. | Plan, existing system, constraints. | Architecture notes and affected files. | Components, data flow, dependencies, and failure modes are understood. | When architecture changes are broad or hard to reverse. |
| Build | Implement the smallest coherent change. | Architecture notes and tasks. | Code, config, docs, or artifacts. | Change matches the plan and avoids unrelated rewrites. | When implementation requires destructive or privileged action. |
| Review | Find defects before validation. | Diff and intent. | Findings, fixes, or approval. | Bugs, regressions, maintainability issues, and scope drift are considered. | When review finds unresolved high-risk issues. |
| Test | Prove behavior with evidence. | Implementation and test plan. | Test results and gaps. | Relevant checks pass or limitations are explained. | When validation cannot run or would affect sensitive systems. |
| Secure | Check trust boundaries and abuse cases. | Implementation, config, dependencies. | Security notes and mitigations. | Secrets, auth, permissions, inputs, outputs, and risky operations are reviewed. | When security impact is uncertain or material. |
| Ship | Prepare delivery. | Reviewed and validated change. | Commit, PR, release notes, deployment plan. | Rollback path and release readiness are clear. | Before production deploys, irreversible actions, or permission changes. |
| Document | Preserve knowledge. | Final behavior and decisions. | Updated docs and decision records. | Users and maintainers can understand the change. | When docs would disclose sensitive details. |
| Handoff | Make continuation easy. | Completed work and validation results. | Handoff notes and next actions. | Next owner can resume without guessing. | When ownership, risk, or next step is unclear. |
