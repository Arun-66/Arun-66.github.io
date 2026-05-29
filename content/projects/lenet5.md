---
layout: project
title: "LeNet-5 FPGA Implementation"
description: "FPGA implementation of the LeNet-5 convolutional neural network for hardware-accelerated image classification."
tags: [FPGA, CNN, LeNet-5, Vitis HLS, Xilinx]
github: "https://github.com/Arun-66/LENET_5"
---

Hardware implementation of LeNet-5 — the classic 5-layer convolutional neural network — on FPGA using Vitis HLS. The project maps the full inference pipeline (convolution, pooling, fully connected layers) onto programmable logic for accelerated image classification.

Key aspects:
- Layer-by-layer HLS kernel design for conv, pooling, and FC operations
- Fixed-point quantization for FPGA-efficient arithmetic
- Dataflow optimization for pipeline parallelism across layers
- Validation against floating-point software reference model
