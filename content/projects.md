---
layout: projects
title: Projects
categories:
  - name: "IC Design"
    entries:
      - title: "Low Phase Noise Quadrature DCO"
        description: "Dual superharmonic injection-locked quadrature DCO in 55nm CMOS for Ka-band LO synthesis. Published at APCCAS 2025."
        tags: [Cadence Virtuoso, SpectreRF, 55nm CMOS, RF]
        link: "https://doi.org/10.1109/APCCAS67402.2025.11376789"
        slug: "quadrature-dco"

      - title: "VCO-Based ADC Architectures"
        description: "Comparative design and analysis of LC-tank vs current-starved VCO-based ADCs. Published at NKCon 2025."
        tags: [Cadence, Mixed-Signal, ADC, SpectreRF]
        link: "https://doi.org/10.1109/NKCon66957.2025.11345792"
        slug: "vco-adc"

      - title: "4-bit Flash ADC"
        description: "Flash ADC architecture using a Wallace Tree encoder for high-speed thermometer-to-binary conversion."
        tags: [ADC, Wallace Tree, Mixed-Signal]
        link: "https://github.com/devesh-b/4bit-Flash-ADC"
        slug: "flash-adc"

      - title: "Tiny Tapeout — Chipalooza"
        description: "Custom ICs submitted to Efabless Chipalooza open shuttle. Received $300 Tiny Tapeout Award (2024)."
        tags: [OpenLane, GDS, Efabless, Digital]
        slug: "tiny-tapeout"

  - name: "Digital Design"
    entries:
      - title: "10BASE-T1S PHY"
        description: "RTL design and functional safety analysis for an automotive Ethernet PHY at Analog Devices India."
        tags: [SystemVerilog, Functional Safety, ISO 26262, ADI]
        slug: "10base-t1s"

      - title: "Dual-Core Lockstep Split Configuration"
        description: "Split configuration architecture for a dual-core lockstep safety processor, implemented during internship at ADI."
        tags: [SystemVerilog, Safety, RTL]

      - title: "Functionally Safe SPI Module"
        description: "SPI peripheral with configurable CPOL/CPHA, error detection, and ISO 26262 safety mechanisms."
        tags: [SystemVerilog, SPI, Functional Safety]

      - title: "Single-Cycle RISC-V Processor"
        description: "Single-cycle RISC-V RV32I processor implemented in Verilog, built and validated for the Computer Organization TA role."
        tags: [Verilog, RISC-V, RIPES, Vivado]
        slug: "risc-v-processor"

  - name: "Software & ML"
    entries:
      - title: "YOLOv8 Hardware Accelerator"
        description: "Investigating algorithmic compression and posit-based approximate computing for hardware acceleration of YOLOv8 inference."
        tags: [Python, Posit, Approximate Computing, FPGA]

      - title: "FMU-NET: Semantic Segmentation for Person ID"
        description: "Novel semantic segmentation architecture for person identification. Published at EASCT 2023."
        tags: [PyTorch, Computer Vision, Segmentation]
        link: "https://doi.org/10.1109/EASCT59475.2023.10392590"
        slug: "fmu-net"
---
