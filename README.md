# Medical AI Governance Gate Demo

A concept demo of a **medical AI governance gate** that prevents AI-generated candidates from being used as-is.

This demo visualizes a simple flow:

**AI candidate generation → ADIC safety check → decision log**

> **Note:** The current UI is designed in **Japanese**.  
> The repository and README can be used internationally, but the on-screen interface text is currently Japanese-first.

---

## What this demo is

This is **not** a drug-checking screen or a generic medical AI UI.

The core idea is different:

- AI may generate candidate options
- a governance layer checks whether they should be allowed to proceed
- unsafe candidates are blocked
- insufficiently supported candidates are returned for human review
- the reason for the decision is recorded

In other words, the point is **not** that AI can suggest options.  
The point is that AI-generated candidates should **not be allowed to pass directly into action without a governance boundary**.

---

## What ADIC does here

In this demo, **ADIC** acts as the core layer that supports:

- checking whether a candidate should be allowed to proceed
- identifying unsafe or under-verified candidates
- returning unclear cases to human review
- recording the basis of the decision

ADIC is presented here as the central component for **check + record**, not as a cosmetic label.

---

## What the demo shows

The demo illustrates three steps:

1. **AI generates candidates**  
   Candidate options are produced from patient-related inputs.

2. **ADIC performs a safety/governance check**  
   Candidates are classified into:

   - **PASS** — acceptable to proceed
   - **BLOCK** — should be stopped
   - **REVIEW** — requires human confirmation

3. **The reason is logged**  
   The demo records why a candidate was stopped, what remains uncertain, and what requires human review.

---

## Why this matters

For medical AI, the key problem is not candidate generation alone.

The real issue is whether a system has a boundary that can:

- stop dangerous outputs
- prevent under-verified suggestions from moving forward
- keep a trace of the decision
- support later explanation and accountability

This is why the demo is positioned as a **medical AI governance** demo rather than a simple recommendation demo.

---

## Included scenarios

The current demo includes the following example scenarios:

- **Scenario A**: Reduced renal function + anticoagulant candidate
- **Scenario B**: Possible pregnancy + anti-infective candidate
- **Scenario C**: Polypharmacy in an older adult + sedation risk

Each scenario shows:

- candidate options
- ADIC check results
- a decision/audit log

---

## Status meanings

- **PASS**  
  A candidate that may proceed

- **BLOCK**  
  A candidate that should be stopped due to risk

- **REVIEW**  
  A candidate that should be returned for human confirmation because information is insufficient or unresolved

---

## Important note

This demo is a **concept demonstration of UI and governance flow**.  
It is **not** a production-ready medical safety engine.

In the current implementation:

- **“Run safety check”** summarizes the currently displayed results and reflects them in the log
- **“Show the safest candidate”** displays a representative PASS candidate

So the demo shows the **structure and logic of governance flow**, not a full real-world safety engine or optimization system.

---

## File structure

This repository is intentionally simple.

- `adic_medical_ai_gate_demo.html`

The demo runs directly in the browser.  
No build process or external dependencies are required.

---

## Intended use

This demo is intended for:

- explaining medical AI governance
- showing the role of ADIC in a decision boundary
- explaining the difference between AI suggestion and governed approval
- PoC presentations
- concept sharing and discussion

---

## Positioning

This is **not** a convenience demo for medical AI features.

It is a demo of a **governance technology that prevents AI-generated medical candidates from being used as-is**.

---

## Rights / notice

The concepts and structure shown in this demo are presented in connection with related disclosed and/or filed technical work.

Please review applicable rights, disclosure status, and usage conditions as needed before redistribution or commercial reuse.

---

## Author / organization

**GhostDrift Mathematical Institute**  
https://ghostdriftresearch.com/