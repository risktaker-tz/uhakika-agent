# Customization Guide

UHAKIKA AGENT is designed to be extended without changing its mission-agnostic core.

## New Skills

Add a skill directory with a `SKILL.md` or follow the upstream template pattern using `SKILL.md.tmpl` where generation is supported. Keep the skill general unless it belongs to a separate project or organization extension.

## New Commands

Add command scripts under `bin/` when the workflow needs reusable local automation. Keep command output clear, deterministic, and safe to run repeatedly.

## New Host Adapters

Add host configuration under `hosts/` and follow the existing host adapter pattern. Define the host root, path rewrites, frontmatter rules, generation rules, runtime sidecars, and install behavior.

## New Workflows

Document workflows under `docs/` and reference the relevant skills, commands, memory files, and quality gates. Workflows should define inputs, outputs, stop conditions, and validation expectations.

## Organization-Specific Extensions

Keep organization-specific policy, style, deployment rules, and compliance requirements separate from the core framework. Prefer an extension directory or clearly named documentation file.

## Project-Specific Extensions

Store project mission, constraints, decisions, risks, and handoff notes in the project memory files. Do not hard-code project-specific assumptions into core skills.

## Safety Rules

Add safety rules in `docs/SAFE_EXECUTION_RULES.md` or an extension-specific safety document. Risky actions should require explicit human approval.

## Review Checklists

Add reusable checklists under `checklists/`. Keep each checklist focused on observable evidence: changed files, validation run, risks documented, rollback path, and next action.
