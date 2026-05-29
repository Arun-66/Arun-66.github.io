---
layout: project
title: "PostgreSQL Acceleration on Alveo U50"
description: "Database accelerator for PostgreSQL workloads on the Xilinx Alveo U50 card using Vitis Libraries."
tags: [Vitis, HLS, Alveo U50, HPC, Database Acceleration]
date: "Jun 2024 – Mar 2025"
---

Designed a hardware database accelerator for PostgreSQL workloads using the Xilinx Alveo U50 data centre card and Vitis Libraries. The project explores offloading database operations to FPGA fabric to reduce query latency and CPU load.

Key aspects:
- FPGA kernel design using Vitis HLS and Vitis Libraries
- Deployment on the Alveo U50 data centre card
- Host-FPGA communication via OpenCL/XRT
- Performance benchmarking against software-only PostgreSQL execution
