---
type: prompt
id: risk-register-entry
title: Risk Register Entry
description: "Creates a structured risk register entry"
tags: [Production, Risk, Quality]
context_params:
  risk_assessment:
    label: "Risk Assessment"
    description: "Scored risk assessment output — the source risks to formalise into register entries."
    required: false
    default_from_previous: true
connections:
  - target: risk-assessment
    type: derived_from
---

Create a formal risk register entry for each risk identified below. Include: risk ID, title, description, category, probability (1-5), impact (1-5), risk score, owner, mitigation actions, contingency plan, and review date.

## Risk Description
{{step.context.risk_assessment}}
