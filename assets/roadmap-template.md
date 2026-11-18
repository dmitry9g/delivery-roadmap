# Development roadmap

Updated: [date, time and timezone]
Goal and final acceptance: [observable outcome]
Authoritative record: [this file, or existing structured state generating this view]
Authorization and constraints: [existing scope, permissions, explicit checkpoints]
Coordinator and ownership: [existing owner; one executor per assignment]
Budget: [authorized active/elapsed caps and deadline, separately from forecasts; accounting method and compliance evidence/gaps, or no user-set cap]

## Optional repair reserve

Include only when useful; a proposed clause is not approval. Existing authorized or uncapped work does not require a new reserve.

Proposed clause for explicit owner approval: “Within [scope/acceptance criteria], I authorize [coordinator and existing team] to diagnose and repair acceptance-blocking defects, verify regressions and the original scenario, perform required Review, integrate and complete the receiving handoff, up to [ceiling and units, accounting method], by [deadline and timezone]. Hard exclusions: [boundaries]. Expected affected files: [forecast, not a hard allowlist unless explicitly stated]. Existing stop instructions, restricted actions, required separate confirmations and other limits remain binding.”

- Status and approval reference: [proposed / approved / paused / exhausted / closed / frozen; owner message/reference]
- Coordinator and current ledger revision: [single owner or supported atomic reservation mechanism]
- Ceiling, units, accounting method and deadline: [approved limits; not an effort forecast]
- Covered scope and activities: [criteria, diagnosis/repair/checks/Review/integration/handoff]
- Hard exclusions and separate permissions: [edit boundaries; paid calls, external actions, recipient/worker limits]
- Actual charges: [settled work only; measurement basis and gaps]
- Open commitments/pending outcomes: [assignment IDs, reserved amounts, owners; uncertainty retained]
- Available balance: [ceiling minus actual charges minus open commitments; unknown if not safely established]
- Next check/stop condition: [whole-cycle allowance and deadline; escalation or resume prerequisites]

Reserve before concurrent dispatch. On verified settlement, replace the commitment with actual charges rather than counting both; release unused allowance only after confirmed settlement/cancellation. Do not reuse closed/frozen balances or treat unknown costs as zero. Reconcile on retry, resume and handoff. Explicit stops and separately required confirmations take precedence.

## Current map

| Step | Current fulfillment | Original estimate | Recorded time | Remaining estimate |
|---|---|---|---|---|
| [stable ID — outcome] | [state; verified scope] | [range, active person-minutes/hours or elapsed minutes/hours, basis] | [active / elapsed / charge, separately labeled; unknown if unmeasured] | [range, active person-minutes/hours or elapsed minutes/hours, condition; or unknown] |

Remaining effort: [active person-minutes/hours; compatible ranges only; identify unestimated work]
Calendar forecast: [elapsed minutes/hours or dated window; dependency/resource-based range with conditions, or unknown]
Next action: [ready step, executor and action; or exact unmet condition]

## Step records

### [Stable ID — outcome]

- Outcome and scope: [affected components/interfaces and intended behavior]
- Executor: [one owner; distinguish assignment from acknowledgement]
- Required review/receiving: [identity and acceptance, or not required]
- Dependencies and inputs: [candidate-specific required predecessors, relevant dependencies/shared resources and availability evidence]
- Acceptance: [observable criteria, relevant failure behavior, required checks]
- Evidence: [artifact/revision/result; reported vs verified; offline vs real]
- Estimate basis/confidence: [known work, uncertainty and reason]
- Recorded time: [role, interval/measurement, active effort / elapsed / accounting charge separately; gaps and cap-compliance evidence if applicable]
- Issues: [finding, affected steps, owner, resolution/mitigation and stop point]
- Next-step readiness: [successor ID: ready / conditional / blocked, reason and evidence; not applicable — already complete when completion evidence remains valid; terminal only when no successor]
- Next action: [next unfinished ready step and prerequisites; skip valid completed successors and avoid duplicate dispatch of running assignments]

## Revision history

| When | Change | Evidence and reason | Impact on scope, dependencies and remaining forecast |
|---|---|---|---|
| [timestamp] | [revision; original baseline retained] | [source] | [consequence] |

Keep history separate from the current map. Split steps retain parent history; do not count both parent rollups and children in totals. Link full logs stored elsewhere.

