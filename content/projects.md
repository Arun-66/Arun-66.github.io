---
layout: projects
title: Projects
categories:
  - name: "FPGA & SoC"
    entries:
      - title: "RISC-V SoC (RV32IM)"
        description: "Full RV32IM core in Verilog with FPGA validation and SoC integration — UART and SPI peripherals, ongoing development."
        tags: [Verilog, SystemVerilog, FPGA, RISC-V, UART, SPI]
        slug: "riscv-soc"
        url: "https://github.com/Arun-66/RISCV_SOC"

      - title: "Dynamic Partial Reconfiguration on FPGA"
        description: "Run-time adaptive reconfiguration of a RISC-V processor's co-processor for resource optimisation using Xilinx Vivado DFX. Built at CHIPS, PES University."
        tags: [Xilinx Vivado, DFX, RISC-V, Partial Reconfiguration, FPGA]
        slug: "dpr-fpga"

      - title: "AES Encryption/Decryption on PYNQ FPGA"
        description: "Hardware-software co-design of AES encryption/decryption on PYNQ-Z2: hardware-accelerated datapath with software-based S-box and key generation."
        tags: [PYNQ-Z2, AES, Verilog, HLS, Hardware-Software Co-design]
        slug: "aes-pynq"
        url: "https://github.com/Arun-66/Cryptographic_Accelerator"

  - name: "Physical Design"
    entries:
      - title: "FIFO — RTL to GDSII"
        description: "Complete RTL-to-GDSII flow for a synchronous FIFO using the Cadence toolchain with SCL180 PDK — synthesis, floorplanning, P&R, timing closure, DRC/LVS."
        tags: [Cadence Genus, Cadence Innovus, SCL180 PDK, GDSII, Physical Design]
        slug: "fifo-gdsii"

      - title: "Digital VLSI Design"
        description: "Implementation of standard digital cells and circuits using Cadence Virtuoso, covering layout, DRC, and LVS verification."
        tags: [Cadence Virtuoso, VLSI, Layout, DRC, LVS]
        slug: "digital-vlsi"
        url: "https://github.com/Arun-66/Digital_VLSI_Design_Cadence"

  - name: "Hardware Acceleration & HPC"
    entries:
      - title: "PostgreSQL Acceleration on Alveo U50"
        description: "Database accelerator for PostgreSQL workloads on the Xilinx Alveo U50 card using Vitis Libraries."
        tags: [Vitis, HLS, Alveo U50, HPC, Database Acceleration]
        slug: "postgres-alveo"

      - title: "LeNet-5 FPGA Implementation"
        description: "FPGA implementation of the LeNet-5 convolutional neural network for hardware-accelerated image classification."
        tags: [FPGA, CNN, LeNet-5, Verilog, HLS]
        slug: "lenet5"
        url: "https://github.com/Arun-66/LENET_5"

  - name: "Tools & Software"
    entries:
      - title: "Arix Assembler"
        description: "Python-based assembler that converts assembly programs to disassembled hex code loadable into instruction memory."
        tags: [Python, Assembly, ISA, Toolchain]
        slug: "arix-assembler"
        url: "https://github.com/Arun-66/Arix_Assembler"

      - title: "QFT Adder"
        description: "Quantum Fourier Transform-based adder implementation, exploring quantum computing approaches to arithmetic circuits."
        tags: [Quantum Computing, QFT, Python]
        slug: "qft-adder"
        url: "https://github.com/Arun-66/QFT_Adder"
---
