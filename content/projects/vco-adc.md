---
layout: project
title: "VCO-Based ADC Architectures"
description: "Comparative design and analysis of LC-tank vs current-starved VCO-based ADCs."
category: "IC Design"
tags: [Cadence, Mixed-Signal, ADC, SpectreRF, VCO]
doi: "10.1109/NKCon66957.2025.11345792"
---

## Overview

VCO-based ADCs exploit a voltage-controlled oscillator as an inherent first-order noise-shaping element: the oscillator phase integrates the input voltage, and a digital counter reads out the phase at each sample clock edge. This work compares two VCO topologies for this application — an LC-tank oscillator and a current-starved ring oscillator — across linearity, noise, power, and area.

## LC-Tank vs. Current-Starved

**LC-tank VCO**: Higher Q at the carrier frequency means lower phase noise floor, which translates to better SNDR for the ADC. The tank also provides a more linear frequency-to-voltage characteristic near the resonant frequency. The main drawback is area: the integrated inductor dominates chip area.

**Current-starved ring VCO**: Compact and fully digital-process-compatible. The ring structure offers wider tuning range, making it easier to cover the full input range. However, the thermal and flicker noise from each inverter stage accumulates, limiting achievable SNDR. At moderate resolutions (8–10 bits, moderate bandwidth), the ring VCO is area-competitive.

## Key Findings

- LC-tank VCO achieves ~8 dB better SNDR at the same power due to the Q advantage
- Ring VCO is viable for applications where area and portability across process nodes outweigh peak noise performance
- The inherent first-order noise shaping is consistent across both topologies; the difference lies entirely in the in-band noise floor

## Publication

Published at **NKCon 2025**.
