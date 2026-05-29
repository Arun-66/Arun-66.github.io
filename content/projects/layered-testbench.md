---
layout: project
title: "Layered Testbench for 4-bit Shift Register"
description: "Structured SystemVerilog verification environment for a 4-bit shift register using a layered testbench architecture."
category: "Digital Design"
tags: [SystemVerilog, UVM-style, Verification, Testbench]
link: "https://github.com/devesh-b/Layered_Testbench_4_Bit_Shift_Register"
---

## Overview

A layered SystemVerilog testbench for a 4-bit shift register, structured around the separation-of-concerns principle that underpins modern UVM-based verification. The testbench decomposes stimulus generation and response checking into discrete, independently reusable layers.

## Testbench Architecture

The five layers each own a distinct responsibility:

**Generator**: Produces randomised or directed transaction objects (shift values, load data, control sequences) without knowledge of the DUT interface.

**Driver**: Translates abstract transactions from the generator into pin-level signal toggles on the DUT interface. Handles timing relative to the clock edge.

**Interface**: A SystemVerilog `interface` block that bundles the DUT signals and provides a clean boundary between the testbench hierarchy and the RTL.

**Monitor**: Passively observes the DUT outputs and packages observed behaviour into transaction objects, mirroring the driver's abstraction level on the output side.

**Scoreboard**: Receives transactions from the monitor and compares them against a reference model prediction to flag mismatches. Maintains pass/fail metrics.

## Outcome

The layered structure enables functional verification methodologies that identify design issues without hand-writing per-signal assertions — coverage-driven stimulus can be dropped in at the generator layer without touching the driver or scoreboard.
