---
layout: project
title: "Flexible CLA Adder"
description: "Modular 4-bit Carry-Look Ahead Adder blocks with scalable architecture for timing and area optimisation."
category: "Digital Design"
tags: [SystemVerilog, Adder, CLA, RTL, Arithmetic]
link: "https://github.com/devesh-b/Flex-CLA"
---

## Overview

A flexible **Carry-Look Ahead (CLA) adder** built from composable 4-bit blocks in SystemVerilog. The CLA topology pre-computes carry signals in parallel rather than rippling through the chain, reducing worst-case addition latency from O(N) to O(log N).

## Architecture

**4-bit CLA block**: Each block computes generate (G) and propagate (P) signals for its bit slice, then resolves carry-out in a single logic level using the standard CLA equations. The block interface exposes carry-in and carry-out, making it directly composable.

**Multi-width variants**: 8-bit, 16-bit, and 32-bit adders are assembled by cascading 4-bit blocks with a group-level CLA. This matches the classic two-level CLA structure used in production arithmetic units.

## Evaluation

Designs were synthesised and benchmarked against ripple-carry and carry-select adder alternatives. The CLA shows the expected timing advantage at wider widths, with the crossover point (where area overhead justifies the speed gain) characterised against the technology library.

Circuit-level simulations confirmed timing closure across process corners.
