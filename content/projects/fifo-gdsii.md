---
layout: project
title: "FIFO — RTL to GDSII"
description: "Complete RTL-to-GDSII flow for a synchronous FIFO using the Cadence toolchain with SCL180 PDK."
tags: [Cadence Genus, Cadence Innovus, SCL180 PDK, GDSII, Physical Design]
date: "Nov 2024 – Dec 2024"
---

Implemented a synchronous FIFO through a complete RTL-to-GDSII physical design flow using the Cadence toolchain and the SCL180 PDK. The project covered every stage of the physical design process from logic synthesis through to a manufacturable layout.

Flow stages:
- **Logic synthesis** — Cadence Genus, timing-driven synthesis with SCL180 standard cell library
- **Floorplanning** — die size, core area, and I/O pin placement
- **Placement and routing** — Cadence Innovus, with congestion and timing awareness
- **Timing closure** — static timing analysis using Cadence Tempus, fixing setup/hold violations
- **DRC/LVS** — design rule check and layout vs schematic verification to achieve a clean, manufacturable layout
