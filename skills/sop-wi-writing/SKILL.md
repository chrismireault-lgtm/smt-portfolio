---
name: sop-wi-writing
description: >
  Use this skill when writing, drafting, or revising any SOP, Work Instruction,
  or controlled procedure document in an ISO 13485 medical device manufacturing
  context. Triggers include: "write an SOP", "draft a work instruction", "update
  the procedure for...", "document this process", or any request to formalize a
  manufacturing or quality process into a controlled document.
---

# SOP / Work Instruction Writing Skill

## Context

Chris is an SMT Process Engineer at a medical device manufacturer operating under
ISO 13485:2016 site certification. Documents must be audit-ready, use IPC and ISO
standard terminology, and conform to a controlled document format.

**Standards baseline:** IPC-A-610H Class 2 · IPC-7711/7721 · J-STD-001 · ISO 13485:2016

---

## Document Type Defaults

| Type | Use When |
|---|---|
| SOP (Standard Operating Procedure) | Process-level, cross-functional, quality system |
| Work Instruction (WI) | Equipment-specific, operator-level, step-by-step |
| Form / Record | Data capture, inspection records, traveler |

When document type is ambiguous, default to **Work Instruction** for anything
equipment- or task-specific, **SOP** for anything process- or system-level.

---

## Document Structure (always follow this)

1. **Header block** — Document number, title, revision, effective date, author, approver
2. **Purpose** — One sentence: what this document governs and why it exists
3. **Scope** — What it covers, what it explicitly does not cover
4. **References** — IPC standards, equipment manuals, related SOPs/WIs by doc number
5. **Definitions** — Any term that could be interpreted differently by a new operator or auditor
6. **Responsibilities** — Who owns each part of the process (by role, not name)
7. **Required Equipment / Materials** — With part numbers or specs where relevant
8. **Procedure** — Numbered steps, imperative voice ("Verify...", "Set...", "Record...")
9. **Acceptance Criteria** — Explicit pass/fail conditions, linked to IPC class where applicable
10. **Records** — What gets recorded, where, retention period
11. **Revision History** — Table: Rev / Date / Description / Author

---

## Writing Rules

- **Imperative voice throughout:** "Inspect the solder joints" not "The operator should inspect"
- **One action per step** — never combine two actions in one numbered step
- **Quantify everything possible** — temperatures, times, pressures, speeds, dimensions
- **IPC references must cite class:** "per IPC-A-610H Class 2" not just "per IPC-A-610"
- **No undefined acronyms** — define on first use, add to Definitions section
- **Avoid passive voice** — "Record the result" not "The result should be recorded"
- **Critical steps get a WARNING or CAUTION callout** — use ISO/ANSI signal word conventions

---

## Output Format

Always output a complete, ready-to-use draft. Do not output an outline or ask
clarifying questions mid-document — make reasonable assumptions, note them at the
top, and flag them for Chris to verify. Use a markdown table for the header block.
