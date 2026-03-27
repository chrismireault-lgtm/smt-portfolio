---
name: npi-process-documentation
description: >
  Use this skill when documenting, planning, or executing any NPI (New Product
  Introduction) process qualification activity on the SMT line. Triggers include:
  "new board coming in", "first article", "qualify this assembly", "NPI build",
  "process qualification for...", or any request to document or plan the
  introduction of a new PCB or assembly into production. Also use when generating
  traveler templates, first-article inspection criteria, or NPI phase checklists.
---

# NPI Process Documentation Skill

## Context

Chris runs NPI qualification end-to-end on an SMT line operating under ISO 13485:2016
and IPC-A-610H Class 2. NPI documentation must support design transfer, first-article
qualification, and eventual production release — all traceable to applicable standards
and defensible in an audit.

**Current NPI phase:** Phase 2 of 7 (Prototype / NPI Builds)

---

## Input Schema

Gather the following before generating any NPI documentation. Flag missing items
rather than assuming:

```
NPI INPUT
─────────────────────────────────────────────
Assembly name / number:    [board or product ID]
Revision:                  [PCB rev and BOM rev]
IPC classification target: [Class 2 / Class 3]
Board complexity:          [layer count, dimensions, component count]
Critical components:       [BGAs, LGAs, fine-pitch, connectors, passives <0402]
New-to-line components:    [any package types not currently in iPulse S20 library]
Paste specification:       [type, alloy, mesh, flux chemistry]
Cleaning requirement:      [yes / no — aqueous post-reflow]
Special processes:         [potting, conformal coat, press-fit, etc.]
Program source:            [new CAD data / conversion from existing / manual]
Target build date:         [NPI build / pilot build]
Open design issues:        [any DFM flags, known pad geometry concerns, etc.]
```

---

## NPI Documentation Framework

Work through these phases in sequence. Generate only what is requested unless
asked for the full package.

---

### Phase 1 — DFM Review

Evaluate the assembly for manufacturability against line capabilities. Flag
issues in three categories:

**Hard stops** — Will cause defects or line incompatibility as-is
- Pad geometry outside IPC-7351 nominal for this class
- Component pitch below iPulse S20 placement capability
- Panel design incompatible with YCP10 or conveyor rail geometry
- Missing or misplaced fiducials

**Recommendations** — Should be addressed before production release
- Pad-to-paste ratio concerns (stencil aperture design risk)
- Thermal relief inadequate for reflow soldering
- Component orientation inconsistencies
- Via-in-pad without fill (thermal wicking risk)

**Watch items** — Monitor during first articles, may not require design action
- Component density affecting cleaning access
- Mixed alloy concerns
- Board finish compatibility with paste chemistry

---

### Phase 2 — Process Parameter Development

Generate first-pass process parameters for each station:

| Station | Parameters to Define |
|---|---|
| YCP10 Screen Printer | Stencil thickness, aperture strategy, squeegee pressure/speed, snap-off |
| Mirtec MS-11E SPI | Inspection program, paste volume limits, offset tolerances |
| iPulse S20 P&P | Placement program, new part library entries, nozzle assignments |
| Heller 1707 MK5 | Reflow profile (ramp, soak, peak, TAL, conveyor speed) |
| Trident LDO Washer | Wash cycle, temperature, dry time (if cleaning required) |

For reflow profiles, cross-reference:
- Paste datasheet process window
- Most thermally sensitive component on the board
- Most thermally massive component on the board
- KIC SPS Smart Profiler validation target

---

### Phase 3 — First Article Inspection Plan

Define the inspection scope for first-article builds:

**100% inspection items** (always)
- Solder joint quality per IPC-A-610H Class 2 (all joints)
- Component presence, orientation, and polarity
- Post-reflow SPI correlation (paste volume vs. joint outcome)

**Sample inspection items** (define AQL based on risk)
- Board dimensions and feature verification
- Cleanliness (if aqueous wash specified)
- Cosmetic / marking requirements

**Critical component inspection** (elevated rigor)
- BGA / LGA: X-ray inspection criteria and accept/reject limits
- Fine-pitch: bridging and coplanarity assessment method
- Any component with a known warpage or thermal risk

---

### Phase 4 — NPI Build Documentation Package

A complete NPI documentation package includes:

1. **Process Parameter Sheet** — All station settings, revision-controlled
2. **Reflow Profile Record** — KIC SPS validation data, attached
3. **First Article Inspection Report** — 100% results, sign-off
4. **New Part Library Record** — iPulse S20 entries for new-to-line components
5. **Stencil Specification** — Thickness, aperture table, material, vendor
6. **DFM Review Record** — Issues found, disposition, design action required
7. **NPI Build Traveler** — Step-by-step build record with sign-off blocks
8. **Open Issues Log** — Unresolved items with owner and target date

---

## Output Defaults

- Default to generating the **Process Parameter Sheet** and **First Article
  Inspection Plan** unless a specific document is requested
- All documents include revision block and effective date placeholder
- Flag any item requiring engineering or quality sign-off
- Note any open design issues that must be resolved before production release
- Use IPC-A-610H class references on all acceptance criteria

---

## Tone and Standards

- Engineering-level precision throughout
- IPC references cite revision and class
- Distinguish clearly between NPI (qualification) and production (released) status
- Any finding with CAPA or design change implications gets flagged explicitly
