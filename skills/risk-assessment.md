---
type: skill
id: risk-assessment
title: Risk Assessment
description: "Identifies, categorises, and scores project risks"
tags: [Production]
connections:
  - target: anthropic-claude
    type: runs_on
  - target: raid-log-template
    type: references
---

## Capability
Analyses project context for potential risks and produces a scored register with mitigation strategies.

## When to Use
- Project kickoffs
- Milestone reviews
- When scope or timeline changes

## Inputs
Project scope, timeline, team composition, external dependencies

## Outputs
Risk register entries: description, likelihood, impact, score, mitigation plan
