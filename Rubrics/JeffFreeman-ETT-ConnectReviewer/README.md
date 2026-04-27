# Jeff Freeman–Style Connect Grader AI Agent

## Overview

This project defines an AI Agent designed to evaluate Microsoft Connect submissions with the same rigor, expectations, and calibration applied by Jeff Freeman when reviewing ETT (Enterprise Technical Team) members at the Principal (L65+) level.

The agent acts as a **deterministic evaluator**, not a writing assistant.  
Its purpose is to **grade Connect submissions for reward readiness**, measurable impact, and alignment with ETT and Microsoft Connect best practices.

The agent is intentionally strict, conservative, and evidence‑based.

---

## The Problem This Solves

### 1. Inconsistent Connect Feedback

Connect reviews often vary depending on:

- Reviewer interpretation
- Writing quality vs. actual impact
- Implicit expectations that are not written down

This leads to:

- Good work being undervalued
- Activity being mistaken for impact
- Frustration during calibration and rewards discussions

### 2. Lack of Measurable, Defensible Scoring

Many Connects describe *what was done* but fail to:

- Quantify outcomes
- Tie work to business value
- Demonstrate scale or reuse

Without structure, Connects become subjective narratives rather than defensible impact statements.

### 3. Principal‑Level Calibration Gaps

At L65+, expectations change:

- Activity is no longer sufficient
- Scale, reuse, and business proxies matter
- Impact must stand up in rewards and calibration discussions

This agent enforces those expectations consistently.

---

## What This Agent Does

The Jeff Freeman Connect Grader AI Agent:

- Evaluates uploaded Connect documents (text, PDF, DOCX)
- Applies **point‑based, deterministic heuristics**
- Scores only what is written (no intent, no assumptions)
- Enforces Principal‑level standards for:
  - Measurable outcomes
  - Business value
  - Scope and scale
  - Delivery excellence
  - Security and quality
  - Cultural behaviors
- Produces:
  - A numeric score (0–100)
  - A grade (A–F equivalent)
  - Criterion‑by‑criterion breakdown
  - Evidence‑based strengths and gaps
  - A confidence level
  - A reward‑readiness recommendation

The same input will always produce the same output.

---

## What This Agent Explicitly Does *Not* Do

- ❌ Rewrite Connect submissions  
- ❌ Add missing metrics or invent impact  
- ❌ Coach, suggest wording, or “make it sound better”  
