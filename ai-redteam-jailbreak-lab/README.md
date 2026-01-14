# AI Red Team Jailbreak Lab

## Overview
This repository documents systematic adversarial testing of conversational AI systems to identify safety, alignment, and instruction-following failures.

The focus of this work is on:
- Jailbreak techniques
- Prompt injection attacks
- Multi-turn manipulation
- Instruction hierarchy confusion
- Bilingual (English–Hindi / Hinglish) safety gaps

All testing is performed manually to simulate real-world adversarial behavior and to ensure reproducibility of findings.

---

## Scope
The project evaluates publicly available conversational AI models, including:
- ChatGPT
- Claude
- Gemini

Testing emphasizes behavioral vulnerabilities rather than model internals.

---

## Methodology
Testing follows a structured red-teaming methodology:
- Hypothesis-driven attack design
- Single-turn and multi-turn adversarial probing
- Linguistic and cultural reframing
- Failure classification using a defined taxonomy
- Reproducible documentation of prompts and responses

Detailed methodology is described in `methodology.md`.

---

## Documentation Standards
Each documented attack case includes:
- Attack objective
- Exact prompt(s) used
- Model responses
- Failure classification
- Severity and reproducibility assessment
- Explanation of risk and impact

---

## Ethics and Responsible Disclosure
This project is conducted strictly for research and educational purposes.

- No automated abuse is performed
- No real-world harm facilitation is intended
- Sensitive content is handled responsibly
- Findings are documented without promoting misuse

See `ethics.md` for details.

---

## Key Findings Summary
This project identifies several systemic weaknesses in conversational AI safety enforcement:

- Authority-based and analytical framing can weaken refusal mechanisms
- Per-turn safety evaluation fails to capture compositional risk across conversations
- Partial disclosure pathways enable indirect reconstruction of disallowed understanding
- Language and cultural framing introduce uneven safety coverage across English and Hindi
- Intent trajectory is underweighted relative to individual prompt evaluation

These findings illustrate why human-led red-teaming remains essential for identifying real-world safety risks that automated benchmarks often miss.

