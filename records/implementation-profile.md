# Skill Implementation Profile

Date: 2026-08-27 | Prepared by: Cody | Status: Release Candidate — Pilot Pending

## Identity And Ownership

- Skill display name: Z Advanced Asana Control
- Canonical skill identifier: `z-advanced-asana-control`
- Owner or publisher: ZedBiz
- Repository: https://github.com/ZedBiz44/z-advanced-asana-control-Skill
- Authoritative branch: `main`
- License or attribution decision: Original ZedBiz material; no third-party runtime code.
- Previous source: `skills/zedbiz-advanced-asana-control` at commit `3fc1a1d1bb0e3273685cb80395f5820fa55a3152`.

## Purpose And Scope

- Primary job: Govern advanced Asana administration through approved agent-owned access.
- Intended users: ZedBiz supervisory agents explicitly approved for the requested Asana scope.
- Positive triggers: Project structure, status or brief publication, shared fields, permissions, portfolios, reporting, workflow redesign, bulk edits, and cross-project changes.
- Requests that must not trigger it: Ordinary assigned-task execution and unrelated read-only navigation.
- Included actions: Inspect, plan, preview, execute, verify, and report approved advanced changes.
- Excluded actions: Credential setup, unauthorized access, silent destructive changes, and regular daily task work.

## Platforms And Packaging

- Supported platform: OpenClaw.
- Authoring source path: Repository root.
- Deployable package path: `dist/z-advanced-asana-control/`.
- Required platform adapters: None.
- Target installation location: Approved OpenClaw workspace skills directory.
- Platform validators: `z-ai-skill-developer` repository validator and `openclaw skills list`.

## Controls And Approval

- Default operating mode: Get-er-Done for bounded changes; Diagnose for controlled changes.
- Human approver: Jack or the project owner delegated by Jack.
- Pilot agents: Marsha for positive and boundary cases; Terry for negative routing checks.
- Wider rollout rule: Pilot and trigger matrix must pass in fresh sessions before fleet rollout.
- Stop conditions: Identity, workspace, permission, GID, confirmation, blast radius, rollback, or verification failure.
- Retry limit: One safe retry for a transient read failure; no blind mutation retry.

## Security And Rollback

- Security review record: `records/security-rollback-review.md`.
- Approved data boundaries: Objects visible through the approved agent PAT in the configured ZedBiz workspace.
- Approved execution boundaries: Only the user's authorized scope; controlled changes require confirmation.
- Last known-good source: Prior skill at commit `3fc1a1d1bb0e3273685cb80395f5820fa55a3152`.
- Rollback owner: Jack or the authorized infrastructure manager.
- Rollback procedure: Remove the release-candidate package and restore the previous installed package from the recorded commit.

## Completion Evidence

- Structural validator result: Pending final repository build.
- Platform validator result: Pending pilot environment.
- Trigger-test record: `records/pilot-test-record.md`.
- Pilot result: Pending.
- Deployed commit or release: Pending.
- GitHub change record: Release-candidate issue to be created.
- Notion operational summary: Z-Advanced-Asana-Control-Skill-SOP.
- Final approver and date: Pending Jack approval after pilot.

