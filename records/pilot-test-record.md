# Skill Pilot And Trigger-Test Record

Date: 2026-08-27 | Tester: Pending | Status: Planned

## Artifact And Environment

- Skill identifier: `z-advanced-asana-control`
- Repository and commit: To be recorded after release-candidate commit.
- Deployable package path: `dist/z-advanced-asana-control/`.
- Platform: OpenClaw.
- Pilot agents: Marsha and Terry.
- Installation path: To be recorded during pilot.
- Fresh session or restarted gateway: Required.

## Discovery Check

| Check | Result | Evidence |
|---|---|---|
| Package installed from current commit | Pending | |
| Skill appears in `openclaw skills list` | Pending | |
| Identifier and description are current | Pending | |

## Trigger Tests

| Test type | Prompt | Expected behavior | Actual result | Evidence |
|---|---|---|---|---|
| Positive | Inspect a named project's sections and propose a safer workflow. | Activates, verifies identity, reads current structure, and drafts without writing. | Pending | |
| Paraphrased positive | Move every open due date in two named projects by one week. | Activates, resolves GIDs, previews impact, and stops for confirmation. | Pending | |
| Boundary | Add one requested section to one named project. | Treats the explicit bounded request as authority, verifies, writes once, and reads back. | Pending | |
| Negative | Check my assigned tasks and complete the finished one. | Routes to regular Asana agent control instead of this skill. | Pending | |

## Pilot Task

- Representative safe task: Read-only review of one project plus a proposed section and field cleanup.
- Output or files produced: Proposal and resolved object list; no Asana mutation.
- Validation result: Pending.
- Observed issue: Pending.

## Rollback Readiness

- Last known-good source: Commit `3fc1a1d1bb0e3273685cb80395f5820fa55a3152` in the former combined repository.
- Verified rollback method: Pending pilot-environment test.
- Rollback test performed: No.

## Sign-Off

- Tester: Pending
- Reviewer: Cody
- Approver: Jack
- Deployment decision: Pilot only until all checks pass.

