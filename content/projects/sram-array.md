---
layout: project
title: "6T SRAM Array"
description: "6T SRAM cell and array designed and laid out in the SkyWater SKY130A PDK, achieving a 5% improvement in read/write stability margins."
category: "IC Design"
tags: [Cadence Virtuoso, SkyWater SKY130A, SRAM, Analog, Layout]
link: "https://github.com/devesh-b/SRAM-Array"
---

## Overview

A 6-transistor SRAM cell and array implementation in the open-source **SkyWater SKY130A PDK**, targeting fabrication-ready layout. The 6T topology is the standard for high-density SRAM — two cross-coupled inverters hold the bit, and two access transistors connect to the bitline pair during read/write.

## Design and Layout

The cell was drawn in **Cadence Virtuoso** with attention to:

- **Symmetry**: the two inverters must be physically matched to prevent static noise margin (SNM) asymmetry
- **Bitline parasitic balance**: matched routing on BL and BLB to avoid read disturb from differential parasitics
- **DRC/LVS clean**: verified against SKY130A design rules before array replication

The cell was arrayed into a small memory macro with row and column decoders.

## Stability Results

PVT (process-voltage-temperature) simulations across SKY130A corner models showed a **5% improvement in read/write stability margins** relative to the baseline cell, achieved through sizing optimisation of the access transistors relative to the pull-down network — the β-ratio tuning that governs the read stability vs write-ability trade-off.
