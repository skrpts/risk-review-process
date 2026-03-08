---
type: workflow
id: risk-review-process
title: Risk Review Process
description: "Identifies risks, scores them, and produces a register update"
tags: [Production]
connections:
  - target: risk-assessment
    type: uses
  - target: risk-register-entry
    type: uses
  - target: milestone-tracker
    type: uses
metadata:
  estimated_duration: "5-15 minutes"
  trigger: manual
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
