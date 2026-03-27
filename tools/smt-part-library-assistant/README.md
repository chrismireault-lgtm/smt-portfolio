# SMT Part Library Assistant

**Type:** HTML (single-file, Anthropic API-powered)  
**Status:** 🔄 Rebuild in progress

---

## Problem

Adding new components to the **Yamaha iPulse S20** part library during NPI required manual datasheet lookup, package geometry extraction, and machine parameter derivation — a slow, error-prone process that created a bottleneck between engineering and production readiness.

## Solution

A standalone HTML application powered by the **Anthropic API**. Accepts a component part number or datasheet and automates the extraction and derivation pipeline, outputting ready-to-use iPulse S20 placement parameters.

## Capabilities

- BOM component lookup by part number
- Datasheet parsing for package geometry and electrical attributes
- iPulse S20 machine parameter derivation:
  - Nozzle type recommendation
  - Pick height and place height
  - Vision recognition parameters
  - Placement speed and force settings
- Output formatted for direct library entry

## Requirements

- Anthropic API key (entered at runtime, not stored)
- Modern browser (Chrome / Edge recommended)
- No server or installation required

## Status

Tool is being rebuilt with updated parameter logic and improved datasheet handling. Will be committed here on completion.

---

*Designed for Yamaha iPulse S20 · Reduces NPI part library build time from hours to minutes*
