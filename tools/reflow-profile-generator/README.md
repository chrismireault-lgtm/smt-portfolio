# Reflow Profile Generator

**Type:** Excel (.xlsx)  
**Status:** 🔄 Rebuild in progress

---

## Problem

Deriving compliant reflow profiles for new paste and component combinations required manually cross-referencing paste datasheets, component thermal limits, and oven zone math — with no structured record of how profile decisions were made.

## Solution

An Excel-based profile generator tuned specifically to the **Heller 1707 MK5** and **KIC SPS Smart Profiler**. Inputs paste specification limits and component thermal constraints; outputs recommended zone temperatures, conveyor speed, and TAL targets with documented rationale.

## Inputs

- Solder paste datasheet limits (preheat ramp, soak window, reflow peak, TAL)
- Critical component thermal limits (max peak temp, max ramp rate)
- Target throughput / conveyor speed constraints

## Outputs

- Zone temperature setpoints (zones 1–7)
- Recommended conveyor speed
- Predicted TAL and peak temp
- Pass/fail margin against paste and component limits
- KIC SPS profile export parameters

## Status

File is being rebuilt for current paste chemistry and component mix. Will be committed here on completion.

---

*Tuned to Heller 1707 MK5 · KIC SPS Smart Profiler · IPC/J-STD-001 compliant profile windows*
