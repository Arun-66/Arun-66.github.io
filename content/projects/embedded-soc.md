---
layout: project
title: "Embedded SoC Design (RV32IM)"
description: "RISC-V SoC with UART, SPI, and QSPI interfaces validated on FPGA using the SkyWater SKY130A PDK."
category: "Digital Design"
tags: [SystemVerilog, C, Cadence Design Suite, RISC-V, SkyWater SKY130A, FPGA]
---

## Overview

A complete embedded SoC built around the RV32IM core — the RISC-V base integer ISA plus the standard multiply/divide extension. The design integrates three peripheral interfaces (UART, SPI, and QSPI) and targets both FPGA validation and physical implementation using the open-source **SkyWater SKY130A PDK**.

## Core and Peripherals

**RV32IM Core**: Implements the full RV32I base instruction set plus the M-extension (integer multiplication and division). The multiplier uses a combinational array multiplier; the divider is an iterative non-restoring design to bound hardware cost.

**UART**: Configurable baud rate, 8N1 frame format, TX/RX FIFOs to decouple the processor from byte timing.

**SPI**: Full-duplex, configurable CPOL/CPHA, chip-select control, master-only mode targeting external flash and sensor interfaces.

**QSPI**: Quad-SPI extension for higher-bandwidth flash communication — four data lines in parallel, supporting single/dual/quad I/O modes for read operations.

## Verification and Implementation

Digital design verification methodologies were applied to ensure functional correctness across all peripheral modes. The design was validated on FPGA (functional correctness and system-level integration) before moving to the SKY130A flow for physical implementation using **Cadence Design Suite**.

The SKY130A flow involved synthesis, place-and-route, and timing closure. The open PDK required careful cell library selection and manual timing constraint tuning to meet target frequencies.
