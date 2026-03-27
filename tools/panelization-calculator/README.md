# PCB Panelization Calculator

**Type:** HTML (single-file, browser-based)  
**Status:** ✅ Active

---

## Problem

During NPI quoting and process planning, calculating panel configurations manually was error-prone and time-consuming. Variables like board spacing, rail geometry, fiducial clearance, and panel yield interact in ways that aren't intuitive to calculate on the fly — especially under time pressure during customer reviews.

## Solution

A self-contained HTML tool that takes board dimensions and panel constraints as inputs and returns a complete panel configuration. No dependencies, no server, no install — opens in any browser.

## Inputs

- Board dimensions (X / Y)
- Panel sheet size
- Board spacing (minimum)
- Rail width (top / bottom)
- Fiducial clearance requirements

## Outputs

- Panel array configuration (rows × columns)
- Board count per panel
- Actual spacing values
- Rail geometry
- Panel yield visualization

## Usage

Open `panelization-calculator.html` in any browser. No installation required.

---

*Built for NPI process planning on a Yamaha iPulse S20 / Yamaha YCP10 line operating to IPC-A-610H Class 2.*
