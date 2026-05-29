---
layout: project
title: "Tiny Tapeout — Chipalooza"
description: "Two custom ICs submitted to Efabless open shuttles. Received $300 Tiny Tapeout Award (2024)."
category: "IC Design"
tags: [OpenLane, GDS, Efabless, Verilog, Analog, Tiny Tapeout]
link: "https://github.com/devesh-b/tt09-deveshb-8-bitMAC"
---

## Tiny Tapeout 9: 8-bit MAC Unit

Submitted to the Tiny Tapeout 9 digital shuttle. The design implements an 8-bit multiply-accumulate (MAC) unit using **Vedic multipliers** and **reversible gates** for energy efficiency.

The architecture splits the 8-bit inputs across the TT input pins and bidirectional I/O using half-clock-cycle multiplexing. The pipeline executes in two half-cycles: multiply in the first, accumulate in the second. Output is serialised through the output and bidirectional pins.

Reversible gates (Toffoli/Fredkin) were used in the adder tree to explore low-power techniques — reversible logic dissipates no energy in theory (Landauer limit). The design was synthesised and hardened using **OpenLane** and submitted to the MPW shuttle via the Efabless platform.

## Tiny Tapeout 9: Universal Active Filter (Analog)

A second TT9 submission on the analog track: a **universal active filter** covering low-pass, high-pass, and band-pass modes with configurable cut-off frequency. Designed collaboratively through PESU-ECC.

## Chipalooza Award

Received the **$300 Tiny Tapeout Award** at the 2024 Chipalooza competition for the analog filter submission — one of ten projects selected from the open shuttle.
