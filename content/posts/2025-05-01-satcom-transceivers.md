---
layout: post
title: "SATCOM transceivers — how they work and where the hard problems are"
date: 2025-05-01
description: A technical overview of satellite communication transceiver architecture, with a focus on Ka-band systems and the open IC design problems that still don't have clean answers.
tags: [RF, SATCOM, circuits, research]
categories: notes
---

Satellite communication has been around long enough to feel solved. It isn't.

The basic picture is familiar: a ground terminal uplinks a modulated RF carrier to a satellite, which amplifies, frequency-shifts, and retransmits it back down to a different ground location. But the IC-level reality — building the transceiver that does this work — involves a tightly coupled set of constraints that get harder, not easier, as the industry moves toward higher frequencies, higher modulation orders, and lower-orbit constellations.

This is a brief technical survey of how Ka-band SATCOM transceivers are structured and where the genuinely open problems sit.

## The basic architecture

Most modern Ka-band ground terminal transceivers use a heterodyne or direct-conversion architecture. The receive chain runs: antenna → LNA → mixer (downconversion from Ka-band to IF or baseband) → variable gain amplifier → ADC → digital baseband. The transmit chain mirrors this, with a PA at the output stage.

At Ka-band (17–21 GHz downlink, 27–31 GHz uplink for most SATCOM allocations), several things become immediately painful.

**Path loss.** Free-space path loss scales as the square of frequency. At 30 GHz you're already fighting roughly 20 dB more loss than at 3 GHz. This puts heavy pressure on both the LNA noise figure on receive and the PA output power and efficiency on transmit. A 1 dB improvement in LNA NF directly improves link margin by 1 dB — which is why the LNA is the most specification-sensitive block in the receive chain.

**Local oscillator phase noise.** The LO is the frequency reference of the transceiver — any phase noise it carries corrupts the demodulated constellation at baseband. An LO that's adequate for QPSK becomes a bottleneck when you're trying to sustain 256APSK, which DVB-S2X now requires for high-throughput terminals. At 30 GHz, even a well-designed PLL accumulates more absolute phase error than at lower frequencies simply because the division ratio from a crystal reference is larger — multiply a 100 MHz reference up to 30 GHz and you've multiplied every noise contribution by 20·log(300) ≈ 49 dB.

**I/Q mismatch.** Direct-conversion architectures are attractive for integration density but sensitive to amplitude and phase imbalance between the I and Q paths. At Ka-band, even small layout asymmetries produce measurable EVM degradation. Calibration helps but costs area and power.

## Technology choices: GaAs vs. CMOS

Until recently, Ka-band SATCOM front-ends were almost exclusively built in GaAs or SiGe BiCMOS — process nodes with high ft/fmax, good PA efficiency, and low noise figures. The cost is integration density: a full transceiver in GaAs is a multi-chip module, not a single die.

The research push of the past several years has been toward standard CMOS implementations. The first Ka-band SATCOM transceiver in standard CMOS was demonstrated by Okada's group at Tokyo Institute of Technology, using a direct-conversion architecture with dual-channel RX for polarization and frequency duplexing [[1]](#references). The motivation is clear: CMOS allows co-integration of the analog RF front-end with the digital baseband, reducing board area, power, and cost — all critical for mass-market LEO terminal scenarios.

The penalty is that CMOS transistors have lower fmax than SiGe HBTs at equivalent nodes, and CMOS PAs suffer efficiency problems at mm-wave due to low supply voltages and lossy substrates. These aren't insurmountable, but they require architectural creativity — stacked PA topologies, transformer-based power combining, and careful LO distribution to manage phase noise across the die.

## The LEO problem

Geostationary satellites sit at 35,786 km and don't move relative to the ground — beam pointing is a one-time calibration. LEO constellations (Starlink, OneWeb, and their successors) orbit at 500–1,200 km. From a ground terminal's perspective, the satellite is continuously moving across the sky. A terminal serving a LEO constellation must use electronically steered phased arrays that can redirect the beam in microseconds.

This changes the transceiver problem significantly. The IC is no longer a single-beam device — it's one element in an array of potentially hundreds, each needing its own phase-shifted LO, its own PA, its own LNA. Per-element power budget becomes extremely tight. A 256-element array at 500 mW per element is a 128 W system — impractical for a consumer terminal. Getting per-element consumption below 50–100 mW while maintaining adequate EIRP and noise figure is an active research problem.

Phase shifter design is another constraint. Analog phase shifters based on varactors or switched networks add noise and nonlinearity. Digital phase shifters quantize phase to discrete steps, introducing quantization lobes in the beam pattern. At Ka-band, 4-bit phase resolution is a common compromise — but whether this is sufficient for high-order modulation in crowded LEO scenarios is still being studied [[2]](#references).

## Open problems

From an IC design perspective, these are the problems without consensus solutions:

**LO synthesis at mm-wave with low phase noise and low power.** A fractional-N PLL synthesizing 30 GHz from a 100 MHz crystal uses a divide ratio of 300. Every noise contribution from the reference and PLL loop filter gets multiplied by ~49 dB. Sub-integer spur management and Σ-Δ quantization noise in the fractional divider both become critical. Injection-locked oscillators and sub-harmonic techniques offer paths to lower power, but at the cost of reduced lock range and less frequency agility [[3]](#references).

**PA efficiency at Ka-band in CMOS.** Power-added efficiency for CMOS PAs at Ka-band typically sits in the 20–35% range, compared to 40–50% achievable in GaAs. For phased-array element budgets, this delta matters enormously. Outphasing, Doherty, and envelope tracking architectures all have mm-wave implementations in the literature, but none has cleanly solved the efficiency-linearity trade-off at the required power levels for high-order modulation.

**Wideband operation for multi-orbit terminals.** A terminal that can serve both GEO (narrow beam, high EIRP, tight phase noise) and LEO (wide scan, lower per-element power, fast frequency switching) has a very different specification set than one optimized for either. The LO synthesizer must cover a wide frequency range while maintaining phase noise performance across the band — a fundamentally difficult combination.

**Doppler in LEO.** A satellite at 7.5 km/s relative to the ground produces significant Doppler shift at Ka-band — on the order of several MHz — that the receiver's carrier tracking loop must acquire and follow continuously. This places requirements on loop bandwidth and VCO tuning range that interact directly with phase noise optimization.

---

My own work on low phase-noise quadrature DCOs at Ka-band [[4]](#references) sits directly in the LO synthesis problem — specifically, using dual superharmonic injection to achieve quadrature accuracy with lower phase noise penalty than conventional approaches. The connection to SATCOM is direct: a cleaner LO means a cleaner constellation, means higher sustainable modulation order, means more bits per second through the link. That is the thread I am following toward doctoral research.

If you are working on related problems — LO design, phased array integration, or CMOS mm-wave circuits — I would be glad to compare notes.

---

## References {#references}

[1] Okada, K. et al., "A Ka-Band CMOS SATCOM Transceiver," *ISSCC 2020*. DOI: [10.1109/ISSCC19947.2020.9063018](https://doi.org/10.1109/ISSCC19947.2020.9063018)

[2] Sadhu, B. et al., "A 28GHz 32-Element TRX Phased-Array IC With Concurrent Dual-Polarized Operation," *ISSCC 2017*. DOI: [10.1109/ISSCC.2017.7870404](https://doi.org/10.1109/ISSCC.2017.7870404)

[3] Analog Devices, "Small Form Factor SATCOM Solutions," *Technical Article*, 2025. [analog.com](https://www.analog.com/en/resources/technical-articles/small-form-factor-satcom-solutions.html)

[4] Bhaskaran, D. and Tantry, S., "Design of a Low Phase Noise Quadrature DCO Using Dual Superharmonic Injection in 55nm CMOS for Ka-Band Applications," *APCCAS 2025*. DOI: [10.1109/APCCAS67402.2025.11376789](https://doi.org/10.1109/APCCAS67402.2025.11376789)
