---
name: z-advanced-asana-control
description: Govern advanced ZedBiz Asana structure, reporting, permissions, bulk changes, and cross-project administration through approved agent access.
---

# Z Advanced Asana Control

Use this skill for advanced ZedBiz Asana administration through the runtime's approved connection.

Use `z-asana-agent-control` for ordinary assigned-task work. Read-only navigation does not need this skill unless it is part of an advanced review.

## 1. Confirm Authority And Route

- **ChatGPT/Codex:** use the connected Asana plugin. A Jack-authenticated connection is the approved route for work Jack requests in ChatGPT.
- **OpenClaw team agent:** use that agent's approved PAT-backed Asana MCP. Do not substitute ChatGPT's connection or another agent's identity.
- Read the connected identity and workspace when the route exposes them. For OpenClaw, require the expected agent email, user GID, and workspace GID. For ChatGPT, verify the requested project/task and intended workspace through the connected plugin.
- Stop if the applicable identity, workspace, tool route, target, or permission cannot be verified.
- Resolve project, task, section, field, option, team, portfolio, and user names to exact GIDs. Do not guess between matches.
- Treat a successful read-only call through the approved route as the connectivity test. A failing legacy probe alone does not prove the route is unavailable.

## 2. Classify The Requested Change

Choose the smallest class that fits the full blast radius.

- **Inspect or draft:** Read structure, diagnose a problem, or prepare a proposed brief, status, workflow, or change set.
- **Bounded change:** A clearly requested, non-destructive change to one project or a small known set of objects.
- **Controlled change:** Bulk edits, cross-project work, permissions, portfolio membership, shared fields, reporting structures, workflow redesign, archive, or delete.

The user's current request is valid authorization for a bounded change when the target and outcome are clear. Do not ask for a second approval merely because the action changes Asana.

Before a controlled change, provide a preview that identifies affected objects, intended values, impact, and rollback method. Obtain explicit confirmation immediately before execution.

Always require explicit confirmation for deletion, archival, permission changes, bulk date shifts, shared-field changes, or changes spanning multiple projects.

## 3. Read Before Writing

Inspect the current object, surrounding structure, fields, dependencies, and permissions needed to judge the change.

Use the narrowest available approved Asana tool. Use a team-membership route only for team or membership operations; use the standard Asana route for ordinary project, task, section, status, story, dependency, and relationship operations.

Do not infer that a missing search result proves an object does not exist or that it is a different object type. Search the relevant object types and respect visibility limits.

## 4. Plan The Change

- Preserve existing structure unless redesign is part of the authorized outcome.
- For sections or task ordering, record current placement and use exact section and neighbor GIDs.
- For fields, inspect the field type, scope, enum option GIDs, and reporting use before editing.
- Add dependencies only for real blocking relationships. Remove them only when resolved or authorized.
- For dates, preserve task duration and dependency logic when required by the request.
- For briefs and status updates, verify project facts and distinguish facts, risks, blockers, decisions, owners, and next actions.
- Prefer reversible operations and state how to undo the change before controlled execution.

## 5. Execute Safely

For a bounded change, execute only the named outcome and affected objects.

For a controlled change:

1. Capture the before-state and affected GIDs.
2. Present the preview and receive confirmation.
3. Apply changes in small verifiable groups.
4. Stop on an unexpected object, permission, field scope, or materially larger impact.
5. Do not continue after a partial failure until the safe state and next action are known.

Do not switch between ChatGPT and OpenClaw authority, use direct REST, or fall back to browser automation when the approved runtime route fails.

## 6. Verify And Report

Read the changed objects back from Asana. Confirm the intended values, placement, relationships, dates, and visibility.

Report:

- what changed and what did not;
- affected projects or objects;
- verification evidence;
- any partial failure, remaining risk, or follow-up;
- rollback status for controlled changes.

Use Asana's automatic activity history as the normal audit trail. Add a human-readable comment or project status only when it helps collaborators or the request requires it. Do not create duplicate audit noise.

Record major structural, bulk, permission, portfolio, shared-field, or reporting changes in the designated technical record. Use Mountain Time for ZedBiz operational timestamps.

## Stop Conditions

Stop before writing when:

- identity, workspace, permission, or target GID cannot be verified;
- the request conflicts with a project owner or Jack's instruction;
- a controlled change lacks its required confirmation;
- the observed blast radius is materially larger than the preview;
- rollback is unclear for a high-impact change;
- Asana returns partial or ambiguous results that prevent verification.

Preserve the safe state, describe the blocker, and request only the missing decision or access.

## Completion Standard

The work is complete only when the approved route and identity were verified, the correct objects were changed, read-back verification passed, and required evidence or escalation was recorded.
