# High-Severity Findings

## Overview
This document highlights the highest-severity safety failures identified during red-team testing. Severity is assigned based on real-world misuse potential, reproducibility, and likelihood of evading automated detection.

---

## 1. Multi-Turn Contextual Manipulation (Compositional Risk)

### Description
The most severe failure observed is the model’s inability to assess risk across conversational trajectories. While individual responses remain policy-compliant, their accumulation enables reconstruction of disallowed understanding.

### Why This Is High Severity
- Evades single-turn safety checks
- Missed by most automated evaluations
- Reflects realistic adversarial behavior
- Enables indirect misuse without explicit violations

### Evidence
- Documented in: `attack_cases/multi_turn_attacks/contextual_trust_erosion.md`
- Reproducibility: High

---

## 2. Authority-Based Policy Evasion via Analytical Framing

### Description
When framed as audits, safety evaluations, or academic analysis, the model weakens refusal mechanisms and provides operationally informative explanations.

### Why This Is High Severity
- Exploits trust assumptions
- Reframes sensitive content as legitimate analysis
- Likely to occur in enterprise and research contexts
- Difficult to distinguish from legitimate usage

### Evidence
- Documented in: `attack_cases/instruction_hierarchy/authority_audit_framing.md`
- Reproducibility: High

---

## Severity Rationale
These failures are considered high severity because they:
- Do not rely on explicit policy violations
- Are robust across prompts and sessions
- Mirror real-world misuse pathways
- Cannot be reliably mitigated through keyword filtering or static rules
