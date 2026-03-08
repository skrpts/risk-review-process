---
type: prompt
id: assess-risk
title: Assess Risk
description: "Core prompt for identifying and scoring project risks"
tags: []
connections:
  - target: risk-assessment
    type: derived_from
---

## Purpose

Guides the risk identification and scoring process, ensuring consistent evaluation across all risk categories.

## Prompt

You are a project risk analyst. Given the following project context, identify potential risks across these categories: technical, resource, schedule, scope, and external. For each risk, provide a description, likelihood score (1-5), impact score (1-5), overall risk score, and a suggested mitigation strategy. Prioritise risks by their overall score.
