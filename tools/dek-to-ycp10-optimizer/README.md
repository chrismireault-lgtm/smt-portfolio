# DEK-to-YCP10 Screen Printer Parameter Optimizer

**Type:** HTML (single-file, browser-based)  
**Status:** 🔄 Rebuild in progress

---

## Problem

Screen printer process documentation in the industry is heavily weighted toward DEK platform terminology and parameter conventions. Translating that knowledge to the **Yamaha YCP10** required manual conversion with no direct reference — creating risk during process development and NPI.

## Solution

A parameter optimization tool that maps DEK process inputs to equivalent Yamaha YCP10 settings, accounting for platform differences in squeegee mechanics, print head design, and vision alignment behavior.

## Inputs

- DEK squeegee pressure (front / rear)
- DEK print speed
- DEK snap-off distance and speed
- Board support / tooling configuration

## Outputs

- YCP10 equivalent squeegee pressure settings
- YCP10 print speed recommendation
- Snap-off parameter translation
- Variance notes where platform behavior differs significantly

## Status

File is being rebuilt with updated parameter mappings. Will be committed here on completion.

---

*Platform translation: DEK → Yamaha YCP10 · IPC-7525 stencil printing process guidelines*
