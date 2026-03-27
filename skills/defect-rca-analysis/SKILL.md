---
name: defect-rca-analysis
description: >
  Use this skill for any SMT defect investigation, root cause analysis, or
  corrective action development. Triggers include: "I'm seeing defects on...",
  "we have a repeatable failure at...", "help me with an RCA for...", "what's
  causing...", or any description of a production or inspection anomaly on the
  SMT line. Also use when reviewing defect data, analyzing SPI or AOI
  rejection trends, or preparing a SCAR or corrective action report.
---

# Defect / RCA Analysis Skill

## Context

Chris runs an SMT line in a medical device manufacturing environment under ISO
13485:2016 and IPC-A-610H Class 2. Defect analysis must be traceable, structured,
and defensible to both internal quality teams and external auditors. Corrective
actions must address root cause, not symptom.

---

## Input Schema

When starting an RCA, gather the following before analyzing. If any are missing,
ask for them before proceeding:

```
DEFECT INPUT
─────────────────────────────────────────────
Component:          [part number / package type]
Board / Assembly:   [PCB reference / assembly number]
Defect type:        [e.g., bridging, open, insufficient, tombstone, shift]
IPC classification: [Class 2 / Class 3 — defect or process indicator?]
Detection point:    [SPI / AOI / visual inspection / functional test / field]
Frequency:          [count / rate / lot size]
Distribution:       [random / positional / lot-correlated / operator-correlated]
First occurrence:   [date or build reference]
Process changes:    [any recent changes to paste, stencil, profile, board rev, P&P program]
Images available:   [yes / no]
```

---

## Analysis Framework

Work through these layers in order. Do not skip to corrective action until
root cause is confirmed or explicitly narrowed to a hypothesis set.

### Layer 1 — Defect Classification
- Classify per IPC-A-610H (defect / process indicator / acceptable condition)
- Identify applicable IPC condition criteria for the package type
- Note any Class 2 vs Class 3 distinction relevant to disposition

### Layer 2 — Process Stage Mapping
Map the defect to its most probable originating process stage:

| Stage | Possible Contributions |
|---|---|
| Paste print (YCP10) | Volume, alignment, release, smear, skip |
| SPI (Mirtec MS-11E) | Measurement offset, false accept, program error |
| Placement (iPulse S20) | Offset, rotation, force, nozzle, feeder |
| Reflow (Heller 1707 MK5) | Ramp rate, peak temp, TAL, delta-T, conveyor speed |
| Board / component | Pad geometry, finish, coplanarity, warpage |
| Material | Paste lot, component lot, shelf life, storage |

### Layer 3 — Cause Hypothesis Generation
Generate hypotheses using the 5-Why or Ishikawa structure. For each hypothesis:
- State the mechanism (how this cause produces this defect)
- Identify what evidence would confirm or eliminate it
- Rate plausibility: High / Medium / Low with reasoning

### Layer 4 — Discriminating Tests
Recommend the minimum set of tests or data pulls to isolate root cause:
- Process data review (SPI trend, profile log, printer CP data)
- Physical inspection (cross-section, SEM, dye-and-pry where applicable)
- DOE recommendation if multiple variables are suspected
- Board / component vendor data request if material cause is suspected

### Layer 5 — Root Cause Statement
Write a formal root cause statement:
> "The [defect type] on [component / location] was caused by [mechanism],
> evidenced by [data / observation], occurring at the [process stage] stage."

---

## Output Schema

Every completed RCA produces these sections:

1. **Defect Summary** — classification, frequency, distribution, detection point
2. **Process Stage Assessment** — where in the process the defect originates
3. **Root Cause Statement** — formal, mechanism-based
4. **Contributing Factors** — secondary causes that compounded the root cause
5. **Corrective Actions** — immediate containment + permanent fix, each with:
   - Action description
   - Owner (by role)
   - Target completion
   - Verification method
6. **Preventive Actions** — process or system changes to prevent recurrence class
7. **IPC Disposition** — accept / rework / reject with IPC reference
8. **Open Questions** — anything requiring additional data before close-out

---

## Tone and Standards

- Engineering-level precision — no hedging, no vague language
- All IPC references cite revision and class: "IPC-A-610H Class 2, Section 7.3"
- Corrective actions are specific and verifiable — never "monitor the process"
- Flag any finding that has audit or CAPA implications
