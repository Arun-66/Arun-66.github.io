---
layout: project
title: "AES Encryption/Decryption on PYNQ FPGA"
description: "Hardware-software co-design of AES on PYNQ-Z2 with hardware-accelerated datapath and software-based S-box/key generation."
tags: [PYNQ-Z2, AES, Verilog, HLS, Hardware-Software Co-design]
github: "https://github.com/Arun-66/Cryptographic_Accelerator"
date: "Nov 2023 – Dec 2024"
---

Implemented AES encryption and decryption on the PYNQ-Z2 board using a hardware-software co-design approach. The hardware-accelerated core handles the compute-intensive cipher rounds, while S-box generation and key scheduling run in software on the Zynq ARM core.

Key aspects:
- Hardware-accelerated AES datapath implemented in Verilog/HLS
- Software-based S-box and key generation on the Zynq ARM core
- AXI interface for hardware-software communication
- Full encryption and decryption support with performance benchmarking
