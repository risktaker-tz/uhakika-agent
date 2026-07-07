# Safe Execution Rules

Agents must not perform risky actions without explicit human approval.

Risky actions include:

- deleting files
- overwriting major architecture
- modifying production configuration
- exposing secrets
- committing credentials
- changing authentication
- changing permissions
- modifying billing/payment settings
- deploying to production
- destructive database operations
- running unknown scripts
- executing irreversible actions

When uncertain, stop, explain the risk, and request approval.
