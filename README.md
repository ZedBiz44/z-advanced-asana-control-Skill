# Z Advanced Asana Control Skill

This repository contains the ZedBiz skill for advanced Asana administration. It governs project structure, reporting, permissions, shared fields, portfolios, bulk changes, and cross-project work performed through approved agent access.

## When To Use

Use this skill when an approved ZedBiz agent must inspect or change advanced Asana structures, create a controlled project-level change, manage dependencies or reporting, or prepare and execute a confirmed bulk or cross-project update.

The authoritative runtime instructions are in [`SKILL.md`](SKILL.md). GitHub is the technical source of truth; the linked Notion SOP is the operational guide.

## Do Not Use

Do not use this skill for ordinary assigned-task work, simple progress comments, or routine completion of an agent's own tasks. Use the regular ZedBiz Asana agent-control skill for that work.

Do not use a personal connector for agent-owned execution. Never store an Asana PAT or another secret in this repository, a prompt, a log, or a test record.

## Safety And Approval

Explicit, bounded, non-destructive requests may proceed without duplicate approval. Deletion, archival, permission changes, bulk date shifts, shared-field changes, and multi-project changes require a preview and explicit confirmation immediately before execution.

The runtime skill must stop on an identity mismatch, unknown GID, unclear permission, larger-than-preview impact, or failed verification.

## Repository Layout

- `SKILL.md` — authoritative runtime rules.
- `records/implementation-profile.md` — ownership, scope, rollout, and completion evidence.
- `records/security-rollback-review.md` — security boundaries and rollback plan.
- `records/pilot-test-record.md` — trigger tests and pilot evidence.
- `package-resources.txt` — approved runtime resource list.
- `scripts/build_package.sh` — builds the deployable package.
- `dist/z-advanced-asana-control/` — generated OpenClaw runtime package.

## Validate And Build

Validate the authoring repository with the validator bundled in `z-ai-skill-developer`:

```bash
python3 /path/to/z-ai-skill-developer-Skill/scripts/validate_skill.py --repository .
bash scripts/build_package.sh
python3 /path/to/z-ai-skill-developer-Skill/scripts/validate_skill.py dist/z-advanced-asana-control
```

The package intentionally contains only `SKILL.md`. Install the tested `dist/z-advanced-asana-control/` directory in the approved OpenClaw skills location, then verify discovery and behavior in a fresh session.

