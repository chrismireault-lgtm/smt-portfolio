# SMT Assembly Cost Model

**Type:** Excel (.xlsx)  
**Status:** 🔄 Rebuild in progress

---

## Problem

Estimating SMT assembly cost for high-volume medical PCB programs required a defensible, structured model that could support both internal planning and capital justification — covering labor, material, rework allowance, and equipment allocation without relying on rough per-board estimates.

## Solution

A comprehensive Excel cost model with tiered volume inputs, component mix complexity factors, and a selective rework strategy overlay. Built for medical PCB programs where cost traceability and defensibility matter as much as the number itself.

## Inputs

- Board complexity (component count, mix of SMD / through-hole / fine-pitch)
- Line rate and shift structure
- Solder paste and consumable costs
- Labor rate (direct / indirect)
- Rework allowance (by defect category)
- Volume tiers (NPI / pilot / production)
- Capital equipment allocation method

## Outputs

- Cost per board by volume tier
- Labor, material, and overhead breakdown
- Rework cost contribution by defect type
- Sensitivity analysis (volume vs. cost curve)
- Capital payback summary

## Status

File is being rebuilt with updated labor rates and volume inputs. Will be committed here on completion.

---

*Used for program quoting and capital justification in an ISO 13485 medical device manufacturing environment*
