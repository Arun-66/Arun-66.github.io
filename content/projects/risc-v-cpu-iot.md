---
layout: project
title: "8-bit RISC-V CPU for IoT"
description: "Energy-efficient 8-bit RISC-V CPU designed for low-power IoT applications and prepared for Tiny Tapeout 9."
category: "Digital Design"
tags: [SystemVerilog, C, Assembly, RISC-V, IoT, Tiny Tapeout, Tapeout]
---

## Overview

An 8-bit RISC-V CPU designed from scratch for low-power IoT applications, with a focus on instruction execution efficiency and minimal area — goals that point toward eventual silicon. The design was prepared for the **Tiny Tapeout 9** shuttle.

## Design Philosophy

Conventional 32-bit RISC-V cores carry more datapath width than most IoT sensor/actuator tasks require. An 8-bit datapath reduces:

- Register file area (eight 8-bit registers vs thirty-two 32-bit)
- ALU gate count
- Memory bus width and associated routing

The instruction set retains enough RISC-V structure to remain programmable in C (via a custom toolchain configuration) and assembly, making it accessible for embedded firmware.

## Implementation

The core was implemented in **SystemVerilog** and firmware was developed in C and RISC-V assembly. Performance analysis covered instruction execution efficiency (IPC, pipeline stall characterisation) and power draw estimates to validate the low-power design goal.

The tapeout-ready version was hardened using the OpenLane flow for submission to the Tiny Tapeout 9 shuttle.
