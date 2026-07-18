---
type: skill
id: risk-register-builder
title: Risk Register Entry
description: "Formatting each scored risk into a formal, structured register entry with owner, mitigation actions, and contingency plan"
tags: [Production, Risk, Quality]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "5 minutes"
  avg_tokens: 3000
  trigger: manual
---

## Risk Register Entry

This skill converts the scored risk assessment into a formal risk register — the structured, documentation-ready deliverable of the risk review process — with one complete entry per identified risk.

### Core Capability

Given the upstream risk assessment (scored risks with likelihood, impact, and initial mitigation suggestions), this skill formalises each risk into a register entry carrying a stable ID, owner, mitigation actions, contingency plan, and review date, ready to drop into project documentation.

### Method

1. **Entry construction:** For each risk in the assessment, create a register entry with risk ID, title, description, category, probability (1-5), impact (1-5), computed risk score, owner, mitigation actions, contingency plan, and review date.
2. **Scoring carry-through:** Preserve the assessment's likelihood and impact scores; compute the overall risk score consistently across all entries.
3. **Prioritisation:** Order entries by overall risk score so the highest-priority risks lead the register.

### Output Structure

A structured risk register — one formal entry per risk, ordered by risk score — ready for project documentation and downstream polishing.
