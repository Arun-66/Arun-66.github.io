---
layout: project
title: "Low Phase Noise Quadrature DCO"
description: "Dual superharmonic injection-locked quadrature DCO in 55nm CMOS for Ka-band LO synthesis."
category: "IC Design"
tags: [Cadence Virtuoso, SpectreRF, 55nm CMOS, RF, Oscillator]
doi: "10.1109/APCCAS67402.2025.11376789"
---

## Overview

This work presents a quadrature digitally controlled oscillator (DCO) designed in TSMC 55nm CMOS targeting Ka-band (26–40 GHz) local oscillator synthesis for SATCOM and mmWave applications. The core technique is dual superharmonic injection locking, which generates accurate quadrature outputs from a single tank oscillator without the power penalty of two separate LC tanks.

## Design Approach

The oscillator uses a class-C topology to improve the power efficiency relative to conventional class-B LC-DCOs. The tank inductor was laid out in symmetric differential configuration to suppress common-mode noise coupling from the substrate. Coarse and fine tuning banks were implemented using switched-capacitor arrays, with binary-weighted coarse steps and thermometer-coded fine steps to suppress the frequency discontinuity at code transitions.

Superharmonic injection locking forces the second harmonic of a half-frequency auxiliary oscillator to lock onto the main tank, producing inherent 90° phase separation. This avoids the divide-by-two quadrature generation approach that typically degrades phase noise by 6 dB.

## Simulation Results

Post-layout SpectreRF simulations (Periodic Steady-State + Periodic Noise) show:

- Phase noise of −112 dBc/Hz at 1 MHz offset
- Tuning range of ~15% relative bandwidth across the Ka-band
- Power draw from a 1.2 V supply

The design was taped out as part of the APCCAS 2025 submission.

## Publication

Published at **IEEE Asia Pacific Conference on Circuits and Systems (APCCAS 2025)**.
