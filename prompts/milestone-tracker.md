---
type: prompt
id: milestone-tracker
title: Milestone Tracker
description: "Analyses milestone progress and forecasts completion"
tags: [Production]
connections:
  - target: burndown-chart-template
    type: references
---

Analyse the following milestone data and produce a traffic-light status report. For each milestone: current status (green/amber/red), percentage complete, days remaining vs estimate, key risks, and recommended actions if off-track.

## Milestones
{{input.timeline}}

## Risk Register Entries
{{steps.risk-register-entry.output}}
