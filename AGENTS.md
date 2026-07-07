# UHAKIKA AGENT - AI Delivery Workflow

UHAKIKA AGENT is a collection of SKILL.md files and host adapters that give AI agents structured roles for planning, building, review, testing, security, documentation, and release readiness.

The framework is mission-agnostic. Users define the mission; UHAKIKA AGENT supplies disciplined verification workflows.

## Available Skills

Skills live in `.agents/skills/` or in host-specific install roots. Some generated paths still use the legacy `gstack` identifier for compatibility with upstream setup, scripts, and syncs.

### Planning

| Skill | What it does |
|---|---|
| `/office-hours` | Clarify goals, constraints, assumptions, and next moves. |
| `/plan-eng-review` | Review architecture, data flow, edge cases, and tests. |
| `/plan-design-review` | Review interaction quality and implementation readiness. |
| `/plan-devex-review` | Review developer experience and workflow friction. |
| `/autoplan` | Run a coordinated planning and review pipeline. |
| `/spec` | Turn vague intent into an executable specification. |

### Implementation And Review

| Skill | What it does |
|---|---|
| `/review` | Pre-landing code review focused on defects and regressions. |
| `/codex` | Request a second-opinion review where supported. |
| `/investigate` | Root-cause debugging before fixes. |
| `/qa` | Browser-backed QA where supported. |
| `/qa-only` | QA report without code changes. |
| `/cso` | Security review using structured threat and risk analysis. |

### Release And Operations

| Skill | What it does |
|---|---|
| `/ship` | Run validation, review, push, and prepare release artifacts. |
| `/land-and-deploy` | Merge, wait for checks, deploy where configured, and verify. |
| `/canary` | Post-release monitoring loop. |
| `/document-release` | Update documentation to match shipped behavior. |
| `/context-save` | Save working context for future continuation. |
| `/context-restore` | Restore saved context after interruption. |

### Browser And Host Integration

| Skill | What it does |
|---|---|
| `/browse` | Browser automation through the upstream browse daemon. |
| `/open-gstack-browser` | Launch the visible compatibility browser command. |
| `/setup-browser-cookies` | Import browser cookies for authenticated testing with user control. |
| `/pair-agent` | Pair another agent with the browser workflow where supported. |

### Safety

| Skill | What it does |
|---|---|
| `/careful` | Warn before destructive or risky commands. |
| `/freeze` | Restrict edit scope. |
| `/guard` | Combine careful and freeze behaviors. |
| `/unfreeze` | Remove directory edit restrictions. |

## Build Commands

```bash
bun install
bun test
bun run test:windows
bun run build
bun run gen:skill-docs
bun run skill:check
```

## Platform Support

- macOS and Linux: full upstream-style test and setup flows are supported.
- Windows: setup expects Git Bash or a compatible POSIX shell. Some validation uses Windows-safe test subsets.

## Key Conventions

- SKILL.md files are generated from templates where `.tmpl` files exist.
- Keep core skills domain-neutral.
- Preserve legacy `gstack-*` command names and `~/.gstack` paths unless performing a dedicated compatibility migration.
- Add UHAKIKA-specific project memory, quality gates, and safety rules as independent extensions.
