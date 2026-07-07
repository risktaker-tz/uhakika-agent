# UHAKIKA AGENT

UHAKIKA AGENT is a verification-first AI agent operating system for planning, building, reviewing, testing, securing, documenting, and shipping high-quality work through disciplined multi-agent workflows.

From idea to verified execution.

## What Is UHAKIKA AGENT?

UHAKIKA AGENT is an independent, general-purpose AI agent operating system derived from the open-source gstack architecture. It preserves the upstream pattern of host adapters, setup automation, Markdown skills, command routing, browser-capable workflows, and validation-oriented delivery while giving this repository its own identity, documentation, and extension layer.

The core system is mission-agnostic. Users define the mission, constraints, success criteria, and risk boundaries for their own project.

## Core Principles

- Certainty comes from disciplined verification, not blind automation.
- Evidence comes before assumptions.
- Quality comes before speed.
- Humans stay in control of risky actions.
- Design, security, testing, documentation, and handoff are part of delivery.
- Agent work should be reviewable, measurable, and reversible.
- Multi-agent coordination is useful only when it improves clarity, safety, or outcomes.

## What It Helps With

- product planning
- requirements clarification
- architecture review
- implementation support
- code review
- QA testing
- browser testing where supported
- security review
- documentation
- deployment readiness
- release planning
- workflow automation
- multi-agent collaboration
- decision support
- operational handoff

## What It Is Not

- not a replacement for human ownership
- not a tool for unsafe unattended execution
- not a guarantee of correctness without review
- not limited to one domain
- not a substitute for security, legal, or operational accountability, but it must always derive user requirements in certain overrides

## Installation

```bash
git clone https://github.com/risktaker-tz/uhakika-agent.git ~/uhakika-agent
cd ~/uhakika-agent
./setup
```

For Codex:

```bash
./setup --host codex
```

Requirements follow the upstream architecture: Git, Bun v1.0+, and the target AI host tooling. On Windows, run setup from Git Bash or an equivalent POSIX shell.

## Host Support

UHAKIKA AGENT keeps the upstream multi-host adapter pattern. Host support is configured under `hosts/` and currently includes Claude Code, OpenAI Codex CLI, OpenCode, Factory, Slate, Kiro, OpenClaw-style dispatch, and related generated skill formats where supported.

Some internal compatibility paths and commands still use the legacy `gstack` identifier, including `gstack-*` command names, `~/.gstack` state paths, and generated skill roots such as `~/.codex/skills/gstack`. These names are preserved intentionally so setup, scripts, and upstream syncs remain compatible.

## Recommended Workflow

Use UHAKIKA AGENT as a disciplined delivery loop:

```text
Clarify -> Plan -> Architect -> Build -> Review -> Test -> Secure -> Ship -> Document -> Handoff
```

For small tasks, a direct fix with focused validation is acceptable. For medium or complex work, create a short plan, identify affected files, document risks, and run appropriate checks before shipping.

## Human-in-the-Loop Safety

Agents must not perform risky actions without explicit human approval. Risky actions include deleting files, overwriting major architecture, modifying production configuration, exposing secrets, changing authentication or permissions, deploying to production, destructive database operations, running unknown scripts, and any irreversible action.

When uncertain, stop, explain the risk, and request approval.

## Upstream Updates

This repository preserves a manual upstream sync path:

```bash
git fetch upstream
git checkout main
git checkout -b sync/upstream-$(date +%Y%m%d)
git merge upstream/main
```

After merging upstream changes, review conflicts carefully, preserve UHAKIKA AGENT branding and custom files, run setup/build/test validation, and merge into `main` only after review. See [docs/SYNC_UPSTREAM.md](docs/SYNC_UPSTREAM.md).

## Customization

UHAKIKA AGENT can be extended with new skills, commands, host adapters, workflows, organization-specific extensions, project-specific extensions, safety rules, and review checklists. See [docs/CUSTOMIZATION_GUIDE.md](docs/CUSTOMIZATION_GUIDE.md).

## License and Attribution

UHAKIKA AGENT includes components derived from the open-source gstack project by Garry Tan and contributors, licensed under the MIT License.

Original upstream: https://github.com/garrytan/gstack

This repository is independently maintained. UHAKIKA-specific branding, documentation, skills, aliases, workflows, and extensions are maintained separately by this repository's maintainers.

See [LICENSE](LICENSE) and [NOTICE](NOTICE).
