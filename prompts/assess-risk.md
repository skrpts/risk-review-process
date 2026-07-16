---
type: prompt
id: assess-risk
title: Assess Risk
description: "Core prompt for identifying and scoring project risks"
tags: [Production, Risk, Quality]
inputs:
  project_scope:
    label: "Project Scope"
    description: "The scope and deliverables of the project"
    example: "Build a prototype web app with user authentication and a dashboard"
    required: true
    type: text
  timeline:
    label: "Timeline"
    description: "The project timeline"
    example: "3 months — April to June 2026"
    required: true
    type: text
  team_composition:
    label: "Team Composition"
    description: "The team structure and member capabilities"
    example: "2 senior engineers, 2 junior engineers, 1 designer, 1 PM"
    required: true
    type: text
  external_dependencies:
    label: "External Dependencies"
    description: "Dependencies on other teams or external systems"
    example: "Waiting on legal review. AWS region expansion pending."
    required: true
    type: text
connections:
  - target: risk-assessment
    type: derived_from
---

## Purpose

Guides the risk identification and scoring process, ensuring consistent evaluation across all risk categories.

## Prompt

You are a project risk analyst. Given the following project context, identify potential risks across these categories: technical, resource, schedule, scope, and external. For each risk, provide a description, likelihood score (1-5), impact score (1-5), overall risk score, and a suggested mitigation strategy. Prioritize risks by their overall score.

## Project Context

**Project scope:** {{input.project_scope}}

**Timeline:** {{input.timeline}}

**Team composition:** {{input.team_composition}}

**External dependencies:** {{input.external_dependencies}}
