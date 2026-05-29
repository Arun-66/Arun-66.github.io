---
layout: project
title: "10BASE-T1S Automotive Ethernet PHY"
description: "RTL design and functional safety analysis for an automotive Ethernet PHY at Analog Devices India."
category: "Digital Design"
tags: [SystemVerilog, Functional Safety, ISO 26262, ADI, Automotive Ethernet]
---

## Overview

The 10BASE-T1S standard (IEEE 802.3cg) defines a 10 Mbps, single-pair automotive Ethernet physical layer supporting multi-drop bus topologies without a dedicated switch. This project involved RTL design and functional safety analysis for a 10BASE-T1S PHY developed at **Analog Devices India**.

## Scope of Work

- Designed RTL modules in SystemVerilog for the PCS (Physical Coding Sublayer) and PMA (Physical Medium Attachment) blocks
- Performed **FMEA (Failure Mode and Effects Analysis)** and derived safety requirements in line with **ISO 26262 ASIL-B** targets
- Implemented hardware redundancy and CRC-based error detection mechanisms to meet the safety integrity requirements
- Contributed to the functional safety architecture document (FSAD) and safety analysis reports

## Functional Safety

ISO 26262 requires that automotive safety-related semiconductor components demonstrate systematic capability at the target ASIL level. For an Ethernet PHY in an ADAS or in-vehicle network context, single-point faults (SPF) and latent faults must be below the ASIL-B diagnostic coverage thresholds. Key mechanisms implemented:

- End-to-end CRC checking with configurable fault reaction
- Redundant state machine encoding for critical path registers
- Loopback test mode for production-time safety mechanism verification

## Context

Work done during employment at **Analog Devices India, Bengaluru**.
