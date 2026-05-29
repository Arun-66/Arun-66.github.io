---
layout: project
title: "AlexNet FPGA Implementation (ZCU104)"
description: "Full AlexNet CNN implemented on the Xilinx ZCU104 using Vitis HLS with layer-by-layer FPGA validation."
tags: [Vitis HLS, ZCU104, AlexNet, CNN, FPGA, Python]
github: "https://github.com/Arun-66/AN50_ZCU104"
---

Implemented AlexNet — a deep convolutional neural network with 5 convolutional layers and 3 fully connected layers — on the Xilinx ZCU104 FPGA using Vitis HLS. The project covers the full pipeline from weight extraction to hardware-validated inference.

Key aspects:
- Layer-by-layer HLS kernel design for convolutional and pooling operations
- Custom Python scripts for weight and bias extraction and formatting into FPGA-loadable files
- TCL scripts for Vitis HLS synthesis and implementation
- Layer output validation by comparing FPGA results against a software reference model
- Deployed on the ZCU104 (Zynq UltraScale+ MPSoC)
