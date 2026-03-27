# SMT Line Overview — Claude Context File
> Paste this file at the start of a Claude session to restore full line context.
> Last updated: 2025

---

## Role & Environment

- **Title:** SMT Process Engineer / Department Lead (sole contributor)
- **Industry:** Medical Device Manufacturing
- **Certification:** ISO 13485:2016 (site-level)
- **Quality Standard:** IPC-A-610H Class 2 (Class 3 build pathway in progress)
- **Rework Standard:** IPC-7711/7721

---

## Production Line Equipment

| Equipment | Make / Model | Notes |
|---|---|---|
| Screen Printer | Yamaha YCP10 | Vision-aligned, closed-loop |
| SPI | Mirtec MS-11E 3D | Post-print, inline |
| Pick & Place | Yamaha iPulse S20 | Multi-gantry, feeder-based |
| Reflow Oven | Heller 1707 MK5 | 7-zone, nitrogen-capable |
| Aqueous Washer | Aqueous Trident LDO | Post-reflow, batch |
| Cleanroom Oven | Sheldon HF | Post-process curing / bake |
| Profiler | KIC SPS Smart Profiler | Reflow validation |

---

## Current Production Context

- **Phase:** NPI / Prototype Builds (Phase 2 of 7-phase roadmap)
- **Open Items:**
  - LGA defect RCA (Silicon Labs BGM11S22F256GA) — stencil aperture increase + PCB rev pending
  - Internal auditor role (volunteered) — cross-functional audit coverage strategy in development
  - SMT audit inclusion — line has not yet been included in internal or external ISO 13485 audits; pre-production qualification documentation in progress
  - Silicone potting feasibility — evaluating in-house capability

---

## Documentation Systems

- **EDMS:** Oracle Fusion (primary), Made2Manage (legacy ERP)
- **CAD:** Altium Designer 23/24
- **Document Control:** WI-C300032 (PCB/PCBA document control work instruction)
- **MES / Traceability:** Evaluating Cogiscan TTC as bridge between ERP and shop floor

---

## Tools Built (in this repo)

- Panelization calculator (HTML)
- Reflow profile generator (Excel / KIC-tuned to Heller 1707 MK5)
- DEK-to-YCP10 screen printer parameter optimizer
- SMT Part Library Assistant (Anthropic API, BOM datasheet lookup + iPulse S20 parameter derivation)
- SMT assembly cost model (Excel, high-volume medical PCB)

---

## Preferred Working Style (for Claude sessions)

- **Thinking style:** Emergent, post-processing — let ideas develop before pushing to resolution
- **Output preference:** Dense, technical, peer-level — no hand-holding, no over-explanation
- **Documentation style:** ISO/IPC-compliant language, structured, audit-ready
- **Problem framing:** Root cause first, then solution — avoid jumping to fixes
- **Terminology:** Use IPC and ISO standard terminology throughout; match existing document conventions

---

## Professional Positioning (for career-related sessions)

- **Target roles:** Senior NPI Process Engineer · Medical Device Manufacturing Engineering Lead
- **Credential pathway:** IPC-A-610 CIS · Six Sigma · ASQ CQE
- **Key differentiators:** Greenfield line build, sole-contributor scope, ISO 13485 environment, process engineering + documentation ownership
