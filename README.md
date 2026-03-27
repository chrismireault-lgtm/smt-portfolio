# SMT Engineering Portfolio
### Process Engineering · Medical Device Manufacturing · IPC-A-610 · ISO 13485

---

## About

I'm an SMT Process Engineer working in medical device manufacturing, operating as a sole-contributor department lead under **ISO 13485:2016** site certification. I built this SMT line from greenfield — owning process engineering, equipment validation, NPI qualification, defect analysis, documentation systems, and continuous improvement end-to-end.

This repository is a working record of the tools, documentation, and frameworks I've developed to run a production-grade SMT line with the rigor that Class 2 medical device assembly demands.

---

## The Line

| Equipment | Make / Model | Role |
|---|---|---|
| Screen Printer | Yamaha YCP10 | Solder paste deposition |
| SPI | Mirtec MS-11E (3D) | Post-print inspection |
| Pick & Place | Yamaha iPulse S20 | Component placement |
| Reflow Oven | Heller 1707 MK5 | Solder reflow |
| Aqueous Washer | Trident LDO | Post-reflow cleaning |
| Cleanroom Oven | Sheldon HF | Post-process curing / bake |

**Standards:** IPC-A-610H Class 2 (Class 3 build pathway in progress) · IPC-7711/7721 · ISO 13485:2016

---

## Tools & Engineering Artifacts

Each tool below was built to solve a real production problem. Source files, documentation, and usage notes are in the linked folders.

---

### 🔧 [`/tools/panelization-calculator`](./tools/panelization-calculator/)
**Problem:** Calculating panel configurations manually was error-prone and slow during NPI quoting.  
**Solution:** Interactive HTML tool that calculates panel yield, board spacing, fiducial clearance, and rail geometry from board dimensions and panel constraints. Runs entirely in-browser with no dependencies.

---

### 🔧 [`/tools/reflow-profile-generator`](./tools/reflow-profile-generator/)
**Problem:** Deriving compliant reflow profiles for new paste/component combinations required manual cross-referencing of paste datasheets, component thermal limits, and oven zone math.  
**Solution:** Excel-based generator tuned to the Heller 1707 MK5 and KIC SPS Smart Profiler. Inputs paste spec and component thermal constraints; outputs recommended zone temps, conveyor speed, and TAL targets with rationale.

---

### 🔧 [`/tools/dek-to-ycp10-optimizer`](./tools/dek-to-ycp10-optimizer/)
**Problem:** Translating screen printer parameters from DEK platform documentation to the Yamaha YCP10 required manual conversion with no direct reference.  
**Solution:** Parameter optimization tool that maps DEK process inputs (pressure, speed, snap-off) to equivalent YCP10 settings, accounting for platform differences in squeegee mechanics and vision alignment.

---

### 🔧 [`/tools/smt-part-library-assistant`](./tools/smt-part-library-assistant/)
**Problem:** NPI parts require datasheet lookup, package validation, and machine parameter derivation before they can be added to the Yamaha iPulse S20 library — a slow, manual process.  
**Solution:** Standalone HTML application powered by the Anthropic API. Accepts a component BPN or datasheet upload, extracts package geometry and electrical attributes, and generates recommended iPulse S20 placement parameters.

---

### 🔧 [`/tools/assembly-cost-model`](./tools/assembly-cost-model/)
**Problem:** Estimating SMT assembly cost for high-volume medical PCB programs required a defensible model covering labor, material, rework allowance, and capital allocation.  
**Solution:** Comprehensive Excel cost model with inputs for board complexity, line rate, component mix, selective rework strategy, and volume tiers. Used internally for program quoting and capital justification.

---

## Documentation

Production-grade SOPs, validation protocols, and engineering templates developed to IPC and ISO 13485 standards.

| Document | Type | Standard |
|---|---|---|
| Post-Reflow Visual Inspection SOP | SOP | IPC-A-610H |
| Yamaha iPulse S20 Operational SOP | SOP | Internal / OEM |
| IQ/OQ/PQ Validation Protocol Framework | Template | ISO 13485 |
| pFMEA Framework | Template | ISO 13485 / AIAG |
| PCB/PCBA Document Control Work Instruction | WI | ISO 13485 |
| SMT Production Roadmap (7-phase, 60-week) | Planning | ISO 13485 |

---

## Engineering Approach

I approach SMT process engineering the same way I approach any complex system: map the failure modes before they find you, build processes that survive operator variability, and document everything as if an auditor walks in tomorrow — because in medical device manufacturing, one eventually does.

What I do well:
- **Greenfield line builds** — equipment selection, validation, and process qualification from zero
- **NPI process engineering** — first-article qualification, stencil design, profile development, acceptance criteria
- **Defect analysis** — root cause identification and corrective action with process-level traceability
- **Documentation systems** — SOP authoring, work instruction development, and audit-ready record structures
- **Cross-functional integration** — bridging engineering, quality, procurement, and ERP systems

---

## Contact

Open to conversations about Senior NPI Process Engineering, Medical Device Manufacturing Engineering Lead, or consulting engagements in SMT process development and line qualification.

📍 Eastern US  
🔗 [LinkedIn](#) *(link forthcoming)*

---

*This repository is actively maintained. Tools and documentation are updated as the line evolves.*
