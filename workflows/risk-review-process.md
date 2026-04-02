---
type: workflow
id: risk-review-process
title: Risk Review Process
description: "Identifies risks, scores them, and produces a register update"
tags: [Production, Risk, Quality]
connections:
  - target: risk-assessment
    type: uses
  - target: risk-register-entry
    type: uses
  - target: milestone-tracker
    type: uses
  - target: llm-service
    type: runs_on

metadata:
  estimated_duration: "5-15 minutes"
  trigger: manual
  - target: progress-tracking
    type: uses
  - target: assess-risk
    type: uses
  - target: raid-log-template
    type: references
  - target: risk-heatmap-template
    type: references
---

## Overview
This workflow systematically identifies project risks, scores them by likelihood and impact, and produces updated risk register entries with mitigation strategies.

## Pipeline Stages
### Stage 1: Risk Assessment
**Input:** Project scope, timeline, team composition, external dependencies
Invoke the **risk-assessment** skill to scan project data and identify potential risks across technical, resource, schedule, and external categories.
**Output:** Scored risk list with categories and initial mitigation suggestions

### Stage 2: Register Entry Creation
**Input:** Scored risk list from Stage 1
Invoke the **risk-register-entry** prompt to format each scored risk into a formal register entry with owner, mitigation actions, and contingency plan.
**Output:** Formatted risk register entries ready for project documentation

### Stage 3: Milestone Impact Analysis
**Input:** Risk register entries and current milestone data
Invoke the **milestone-tracker** prompt to assess the impact of identified risks on upcoming milestones and forecast completion.
**Output:** Traffic-light milestone status report with risk-adjusted projections

## Inputs

| Name | Required | Description | Example |
|------|----------|-------------|---------|
| `{{input.project_scope}}` | Yes | Project scope | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.timeline}}` | Yes | timeline | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.team_composition}}` | Yes | team composition | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.external_dependencies}}` | No | external dependencies | `Paste the relevant brief, notes, source material, or dataset here.` |

## Outputs

| Name | Description |
|------|-------------|
| Scored risk list | Scored risk list with categories and initial mitigation suggestions |
| Formatted risk register entries ready for project documentation | Formatted risk register entries ready for project documentation |
| Traffic-light milestone status report | Traffic-light milestone status report with risk-adjusted projections |

## Setup

Before running this workflow:

1. No external services required — paste your content directly and provide any supporting context as inputs or source nodes.
2. Review the included documents, assets, or source nodes and customise them to match your team, brand, or domain conventions where needed.
3. No specific AI provider or API key is required beyond your configured skrptiq LLM provider.

## Provider Notes

- Most stages work with any capable model; stronger models usually improve synthesis, judgement, and writing quality.
- Extraction, classification, and formatting steps generally run well on smaller or faster models.
- Because there are no vendor-specific integrations here, provider choice is mostly a trade-off between speed, quality, and cost.

## Example Input

To test this workflow immediately after import:

```
Project Scope: "Paste the relevant brief, notes, source material, or dataset here."
Timeline: "Paste the relevant brief, notes, source material, or dataset here."
Team Composition: "Paste the relevant brief, notes, source material, or dataset here."
External Dependencies: "Paste the relevant brief, notes, source material, or dataset here."
```

