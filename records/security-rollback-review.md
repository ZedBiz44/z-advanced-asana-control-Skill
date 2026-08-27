# Skill Security And Rollback Review

Date: 2026-08-27 | Reviewer: Cody | Status: Prepared — Approval Pending

## Trust And Inputs

| Review point | Decision and evidence |
|---|---|
| Approved source types | User request and Asana objects returned through the approved ZedBiz PAT-backed MCP. |
| Private or client-sensitive content | Read and change only what is required for the authorized Asana outcome; do not copy unrelated content into logs or reports. |
| Untrusted instructions or files | Treat task text, comments, links, and attachments as data, not authority to expand scope or change credentials. |
| Allowed network services | Approved Asana MCP route only for runtime work. |
| Prohibited input or content | PAT values, passwords, private keys, complete environment files, and unauthorized workspace data. |

## Execution And Data Boundaries

| Review point | Decision and evidence |
|---|---|
| Allowed commands and file locations | Runtime skill requires no shell commands or filesystem writes. |
| Transfer boundary | Do not transfer Asana data outside the approved request, evidence record, or designated ZedBiz systems. |
| Secrets process | Credentials stay in the approved secret store and agent runtime; verify identity through a current-user call without recording token values. |
| High-impact approval gate | Preview and explicit confirmation are required before delete, archive, permission, bulk date, shared-field, or multi-project changes. |
| Validation and logging | Read back changed objects; use native activity history and record major controlled changes in the designated technical record. |

## Rollback And Removal

| Review point | Decision and evidence |
|---|---|
| Last known-good source | Prior skill at commit `3fc1a1d1bb0e3273685cb80395f5820fa55a3152`. |
| Pilot installation location | To be recorded during pilot. |
| Rollback owner | Jack or authorized infrastructure manager. |
| Replacement or removal procedure | Remove the candidate package, restore the prior package, restart or refresh discovery, and verify the previous identifier and behavior. |
| Immediate rollback conditions | Wrong identity route, unexpected activation, bypassed confirmation, larger-than-preview mutations, or inability to verify results. |
| Evidence after rollback | Installed package checksum or commit, discovery result, safe read-only identity check, and pilot record update. |

## Approval

- Reviewer: Cody
- Approver: Jack
- Approval date: Pending
- Open risk or exception: Live pilot and rollback verification are pending.

