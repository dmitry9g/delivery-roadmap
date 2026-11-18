---
name: delivery-roadmap
description: Create and maintain development roadmaps with verified fulfillment, original estimates, recorded time, remaining forecasts, and next-step readiness. Use when asked to create or update a roadmap, report progress against an existing roadmap, replan from evidence, or advance an approved roadmap.
---

# Delivery Roadmap

Maintain a compact current plan that supports confident implementation and automatic continuation within existing authorization. Preserve the user's goal, acceptance criteria, constraints, ownership and budgets. Approval to create or maintain a roadmap does not itself authorize implementation or external actions.

## Establish the current plan

For a standalone status question, report the available status without creating a roadmap unless the user asks for one. Reuse the authoritative roadmap and existing assignments. Inspect only evidence needed to establish fulfillment, blockers and ownership. Distinguish delivery, acknowledgement, execution, review and acceptance; an assignment or unverified worker claim does not establish completion.

For a new roadmap, adapt [assets/roadmap-template.md](assets/roadmap-template.md). Maintain one authoritative current state, with a compact revision history separate from that state. Update existing records in place instead of accumulating competing current snapshots. If existing automation uses structured state, derive the human view from it. Do not introduce another datastore just for this skill.

In roadmap reports, always show **Step, Current fulfillment, Original estimate, Recorded time, Remaining estimate**. Preserve stable step IDs. Keep **Next-step readiness** in each supporting step record; surface it in the main table when it explains a blocker or next action. Avoid subjective percentage completion.

## Size steps for confident implementation

Each step needs a coherent outcome, identifiable affected components/interfaces, acceptance evidence, dependencies, one accountable executor and an estimate with a stated basis. Include relevant verification, review, integration and handoff. Follow required review policy without inventing independent review for every trivial change.

If an important assumption is unresolved, first define a bounded investigation with a specific question, evidence to collect and decision to produce. Split steps when this reduces uncertainty, isolates ownership or permits useful verification. Keep coupled changes together when separation creates incomplete interfaces. Do not impose universal duration, file-count or step-count limits.

Record outcome, scope, acceptance criteria, evidence, owner, required reviewer/receiver, dependencies, estimate confidence and its reason, issues and next action. Distant uncertain work may remain a coarse milestone; refine it before dispatch. Avoid speculative microtasks.

## Fulfillment and next-step readiness

Use states such as **planned, ready, implementing, awaiting review, blocked, complete**, with concrete scope qualifiers such as “offline behavior accepted; real execution unverified.” Complete means the planned outcome, required checks/review and receiving acceptance are evidenced. Source inspection or mocks do not establish real operation; component success does not establish integration success.

Every step identifies its successor(s) and records readiness:

- **Ready:** all progression conditions below are evidenced for that successor.
- **Conditional:** a named check or prerequisite remains unresolved; dependent execution must wait.
- **Blocked:** a known unmet condition prevents progression; name its owner and resolution.

Before dispatch, reconcile each candidate successor with its current state and evidence. Skip a successor whose completion evidence remains valid, mark its readiness “not applicable — already complete,” and assess the next unfinished dependent step. Do not duplicate work already assigned and running. Use “not applicable — terminal step” only when no successor remains. Record readiness separately for branches. A completed step may have a blocked successor.

For each unfinished candidate, confirm:

1. Its required predecessors satisfy their acceptance criteria and required review/receiving.
2. Its inputs, outputs, interfaces and assumptions remain compatible with relevant dependencies and downstream requirements; affected failure, cancellation and recovery behavior is covered where relevant.
3. No known unresolved issue threatens this candidate or the required final outcome through this candidate without adequate, evidenced mitigation.
4. Inputs, dependencies, ownership and execution/review capacity are available.
5. The next actions fit existing scope, permissions and remaining budget, including verification and reporting.

Unrelated unfinished work does not block a candidate unless it creates an actual dependency, shared-resource conflict or constraint. Assess foreseeable material risks, not hypothetical proof that no future defect is possible. Reuse valid evidence and run affected checks; avoid repeating healthy full suites without a reason. Deferred issues require an owner, affected steps, resolution plan and stop point. They cannot silently pass a gate they threaten.

## Continue within authorization

When execution is authorized and the progression conditions pass, record completion, refresh the roadmap and start the next ready step without another “continue.” Honor explicit pause and checkpoint instructions. Keep one executor per assignment and coordinate shared resources through the existing owner. A roadmap does not authorize extra workers or recipient messages.

- Repair defects within existing scope and budget, verify, then reassess readiness.
- When one branch is blocked, continue an already authorized independent branch if ownership and resources permit. Do not bypass the blocked dependency.
- When evidence undermines the approach, revise affected steps before more dependent work. Repeated failures warrant checking the underlying assumption instead of repeating the same attempt.
- Ask only for a necessary user decision or expanded authority, such as changed scope, exceeded budget or a restricted action. State the exact unmet condition and smallest actionable decision.

At interruption, leave the exact next action and restart prerequisites. This skill does not create a scheduler or background worker; claim unattended continuation only when an authorized execution mechanism exists.

## Use an owner-approved repair reserve

When a defect blocks an approved acceptance criterion, first check whether existing authority covers the repair. An optional repair reserve can make that authority explicit in the plan; this skill and an unapproved template grant none. Do not introduce a new approval gate for work already authorized, or invent a reserve for uncapped work.

Keep the reserve in the authoritative roadmap, not a separate budget. Record the owner's approval reference, accountable coordinator, authorized ceiling and accounting units, expiry/deadline, covered acceptance criteria and repair activities, hard exclusions, commitments, actual charges and available balance. Distinguish expected affected files (a forecast) from hard edit boundaries (an authorization constraint). A newly discovered file alone does not require escalation unless it crosses an approved boundary.

An explicitly approved clause may cover diagnosis, implementation, regression/original-scenario verification, required Review, integration and receiving handoff within its limits. Dispatch those covered actions without another generic acknowledgement, but reserve enough allowance for the whole repair cycle, including review and reporting. It does not authorize extra workers, recipients, paid calls, publication or other external actions unless separately covered by existing authority.

Before dispatch, retry, resume or handoff, reconcile the current ledger and pending outcomes through its single coordinator or supported atomic reservation mechanism. Available balance is the authorized ceiling minus actual charges and still-open commitments in compatible units; do not subtract a settled commitment twice. For resumed work, reconcile and reuse its valid existing commitment; reserve only an uncovered increment rather than charging the same work twice. Reserve allowance before concurrent work, replace its commitment with actual charges on settlement, and release unused allowance only after verifying that the work is settled or cancelled. Unknown or pending charges are not zero or refundable capacity. If safe remaining capacity cannot be established, block spending from that reserve while continuing independent permitted work.

Stop the affected repair and request the smallest necessary decision when the remaining allowance cannot cover its completion, the deadline would be exceeded, a hard exclusion would be crossed, or the goal/acceptance criteria would change. Preserve work and state; do not reset caps on retries, borrow another task's allowance, or reopen closed/frozen balances without owner authority. An explicit pause or stop takes precedence even when balance remains. A reserve never overrides restricted or denied actions, platform safeguards, or separately required action-time confirmations. Do not automatically retry a denied action.

## Keep estimates and time honest

Preserve original estimates and their basis; update remaining forecasts separately. Label every estimate, including remaining estimates, with explicit active person-minutes/hours or elapsed minutes/hours. Use ranges and explain uncertainty. Keep expected effort (forecast), authorized maximum (cap) and recorded expenditure separate; a cap is not a forecast. Distinguish **measured active effort**, **elapsed duration** and **conservative accounting charge**. Unknown time remains unknown, not zero. An allocation or wall interval is not measured active effort. Include author, reviewer, coordinator and reporting effort when the budget covers them.

Sum only compatible, non-overlapping records. Parallel workers' active effort may add while elapsed intervals overlap. Do not count parent and child totals together or charge cross-project work twice. Re-estimate remaining work from evidence rather than subtracting elapsed time from an active estimate.

When a cap applies, state the accounting method and the evidence supporting compliance. An allocation or unmeasured accounting charge does not establish that measured effort stayed within the cap; identify missing measurements and limit the claim accordingly. Do not invent a cap for uncapped work.

Separate remaining effort from calendar forecast. Use dependency order, shared resources and reviewer availability for calendar estimates; make forecasts conditional or unknown when necessary. An attempt cutoff is not a delivery promise. Honor user-set aggregate caps and deadlines across retries. Do not reset clocks or reuse closed/frozen balances without authority, and do not invent caps or approval gates when none were set.

## Correct and report

For material revisions, record **change → supporting evidence → reason → impact on scope, dependencies and remaining forecast**. Preserve the original baseline and historical work. Splitting a step retains its parent ID/history and allocates existing time once; label parent rollups to avoid double counting. Mark newly scoped work without a historical estimate as new rather than inventing a baseline.

Reassess downstream readiness when evidence or interfaces change. Reopen affected completion claims if acceptance evidence is invalidated. Routine corrections within authorized scope need no additional approval.

After a completed step, material blocker or justified revision, show the full compact roadmap, recorded time and updated remaining effort/calendar forecast. Lead with what changed, the next executable action and any necessary decision. Link long evidence rather than copying logs. Keep reporting proportionate to the work and avoid repeated unchanged updates.

