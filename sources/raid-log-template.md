---
type: source
id: raid-log-template
title: RAID Log Template
description: "Template for Risks, Assumptions, Issues, Dependencies tracking"
tags: [Production, analysis:risk, quality:standards]
connections: []
---

## RAID Framework Overview

RAID is a structured approach to tracking four categories of project uncertainty:

- **Risks** — events that have not yet occurred but could negatively affect the project if they do. Risks are prospective: they require proactive planning and mitigation.
- **Assumptions** — conditions believed to be true for planning purposes but not yet confirmed. If an assumption proves false, it typically generates a new risk or issue.
- **Issues** — problems that have already occurred and require resolution. Unlike risks, issues are active and demand immediate or near-term action.
- **Dependencies** — external factors, deliverables, or decisions the project relies upon but does not directly control. A missed dependency often becomes an issue.

The RAID log is a living document. It should be reviewed regularly, updated as the project evolves, and used as a standing agenda item in governance meetings.

## Risk Scoring Matrix

Every risk is scored on two dimensions: **Likelihood** (how probable) and **Impact** (how severe if it occurs). Multiply the two scores to produce a **Risk Score** (1–25).

### Likelihood Scale

| Score | Level | Definition |
|-------|-------|------------|
| 1 | Rare | Less than 10% probability; would require exceptional circumstances |
| 2 | Unlikely | 10–30% probability; possible but not expected |
| 3 | Possible | 30–60% probability; could reasonably occur |
| 4 | Likely | 60–85% probability; more likely to occur than not |
| 5 | Almost certain | Greater than 85% probability; expected to occur |

### Impact Scale

| Score | Level | Definition |
|-------|-------|------------|
| 1 | Negligible | Minimal effect on timeline, cost, or quality; absorbed within normal tolerances |
| 2 | Minor | Small schedule slip (days) or minor cost increase; workaround available |
| 3 | Moderate | Noticeable schedule delay (1–2 weeks) or budget overrun (5–10%); requires management attention |
| 4 | Major | Significant schedule delay (weeks to months) or budget overrun (10–25%); affects project objectives |
| 5 | Critical | Project objectives at serious risk; potential for project failure, major reputational damage, or regulatory breach |

### Risk Rating Thresholds

| Risk Score | Rating | Action |
|------------|--------|--------|
| 1–4 | Low (green) | Monitor; review monthly |
| 5–9 | Medium (amber) | Active mitigation plan required; review fortnightly |
| 10–16 | High (red) | Escalate to project sponsor; mitigation underway; review weekly |
| 17–25 | Critical (black) | Immediate escalation to steering committee; emergency response |

## Risks Template

| Field | Description |
|-------|------------|
| **ID** | Unique identifier (e.g. R-001) |
| **Date raised** | When the risk was first identified |
| **Raised by** | Person who identified the risk |
| **Description** | Clear statement of the risk event and its potential consequence |
| **Category** | e.g. Technical, Resource, Commercial, Regulatory, Operational |
| **Likelihood** | 1–5 (see scale above) |
| **Impact** | 1–5 (see scale above) |
| **Risk score** | Likelihood × Impact |
| **Mitigation strategy** | Actions planned to reduce likelihood or impact |
| **Contingency plan** | What to do if the risk materialises despite mitigation |
| **Owner** | Person accountable for managing the risk |
| **Status** | Open / Mitigated / Closed / Escalated |
| **Review date** | Next scheduled review |

### Example Risk Entry

> **R-003** | Raised 15 Jan 2025 by J. Patel
> *Key supplier may not deliver API integration by the March deadline.*
> Category: Technical | Likelihood: 3 (Possible) | Impact: 4 (Major) | Score: 12 (High)
> **Mitigation:** Weekly check-ins with supplier; parallel evaluation of alternative provider.
> **Contingency:** Switch to alternative provider; accept 2-week schedule extension.
> **Owner:** T. Okafor | **Status:** Open | **Next review:** 29 Jan 2025

## Assumptions Template

| Field | Description |
|-------|------------|
| **ID** | Unique identifier (e.g. A-001) |
| **Date raised** | When the assumption was first recorded |
| **Description** | The condition assumed to be true |
| **Impact if invalid** | What happens to the project if this assumption proves false |
| **Validation approach** | How and when the assumption will be confirmed or disproved |
| **Owner** | Person responsible for validating the assumption |
| **Status** | Open / Validated / Invalid / Closed |

### Example Assumption Entry

> **A-005** | Raised 10 Jan 2025
> *Budget approval for Phase 2 will be granted by end of Q1.*
> **Impact if invalid:** Phase 2 start delayed by at least one quarter; team may be redeployed.
> **Validation:** Finance board meeting scheduled 28 Feb 2025.
> **Owner:** S. Morgan | **Status:** Open

## Issues Template

| Field | Description |
|-------|------------|
| **ID** | Unique identifier (e.g. I-001) |
| **Date raised** | When the issue was identified |
| **Raised by** | Person who flagged the issue |
| **Description** | Clear statement of the problem |
| **Impact** | Effect on timeline, cost, quality, or scope |
| **Priority** | Critical / High / Medium / Low |
| **Resolution plan** | Actions being taken to resolve the issue |
| **Owner** | Person accountable for resolution |
| **Status** | Open / In progress / Closed / Escalated |
| **Target resolution date** | When the issue should be resolved by |

### Example Issue Entry

> **I-007** | Raised 22 Jan 2025 by A. Chen
> *Test environment has been unavailable for 3 days due to infrastructure failure.*
> **Impact:** Testing blocked; 3-day delay to sprint delivery.
> **Priority:** High
> **Resolution:** Infrastructure team restoring from backup; ETA 24 Jan.
> **Owner:** R. Okeke | **Status:** In progress | **Target:** 24 Jan 2025

## Dependencies Template

| Field | Description |
|-------|------------|
| **ID** | Unique identifier (e.g. D-001) |
| **Date raised** | When the dependency was identified |
| **Description** | What the project depends on |
| **Source** | The external team, system, or organisation providing the dependency |
| **Required by** | The date by which the dependency must be fulfilled |
| **Impact if missed** | Consequence of the dependency not being met on time |
| **Owner** | Person responsible for tracking and chasing the dependency |
| **Status** | Open / On track / At risk / Delivered / Missed |

### Example Dependency Entry

> **D-012** | Raised 5 Jan 2025
> *Legal team to complete data processing agreement with third-party analytics provider.*
> **Source:** Legal department
> **Required by:** 1 Mar 2025
> **Impact if missed:** Analytics integration cannot go live; launch delayed.
> **Owner:** K. Nakamura | **Status:** On track

## Status Definitions

| Status | Meaning |
|--------|---------|
| **Open** | Identified and being monitored; no resolution action yet |
| **In progress** | Active work underway to resolve or mitigate |
| **Mitigated** | (Risks only) Mitigation actions have reduced the risk to an acceptable level |
| **Validated** | (Assumptions only) Confirmed to be true |
| **Invalid** | (Assumptions only) Proven false; likely triggers a new risk or issue |
| **On track** | (Dependencies only) Expected to be delivered on time |
| **At risk** | (Dependencies only) Delivery timeline is uncertain; needs attention |
| **Delivered** | (Dependencies only) Received as expected |
| **Missed** | (Dependencies only) Not delivered by the required date |
| **Escalated** | Raised to a higher authority (project sponsor or steering committee) for decision |
| **Closed** | Fully resolved or no longer relevant |

## Review Cadence

- **Weekly:** Review all High and Critical risks, all open issues, and any at-risk dependencies. Update scores and statuses.
- **Fortnightly:** Full RAID log review covering all categories and all statuses. Validate or close assumptions. Re-score risks where circumstances have changed.
- **Monthly:** Summary report to project sponsor highlighting new items, score changes, escalations, and closures.
- **Milestone / phase gate:** Comprehensive RAID review before any major phase transition or go/no-go decision.

## Escalation Criteria

Escalate to the steering committee when any of the following conditions are met:

- A risk scores 17 or above (Critical rating)
- A risk score increases by 6 or more points between reviews
- An issue remains unresolved past its target resolution date by more than one week and is blocking a critical path activity
- A dependency is formally missed and affects the project's milestone schedule
- An assumption is proven invalid and the resulting impact is rated Major (4) or Critical (5)
- Cumulative effect of multiple Medium risks exceeds a combined score threshold agreed at project initiation (commonly 30+)

When escalating, provide: the RAID item ID, a concise description, the current score or status, the action requested from the committee, and a recommended course of action.
