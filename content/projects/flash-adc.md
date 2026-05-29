---
layout: project
title: "4-bit Flash ADC"
description: "4-bit Flash ADC architecture using a Wallace Tree encoder for high-speed thermometer-to-binary conversion."
category: "IC Design"
tags: [ADC, Flash ADC, Wallace Tree, Verilog, Mixed-Signal]
link: "https://github.com/devesh-b/4bit-Flash-ADC"
---

## Overview

A 4-bit flash ADC architecture where all 15 comparator outputs are resolved in parallel, making flash conversion the fastest ADC topology. The thermometer code output (15 bits for a 4-bit ADC) is converted to binary using a **Wallace Tree encoder** rather than a ROM-based priority encoder, reducing the propagation delay through the encoding stage.

## Architecture

**Comparator bank**: 15 differential comparators, each with a reference voltage at a different tap of the resistor ladder. All comparators resolve simultaneously.

**Wallace Tree encoder**: A Wallace tree is a carry-save adder network that reduces the partial products (or in this case, thermometer bits) in a tree structure. For ADC encoding, it accepts the 15 thermometer bits and produces a 4-bit binary output with fewer adder stages than a ripple-carry encoder, improving throughput at high sampling rates.

## Trade-offs

- Flash ADCs trade area and power for speed — 15 comparators vs 1 for a successive approximation design
- The Wallace Tree encoder reduces encoding latency at the cost of irregular routing
- At 4 bits, the comparator mismatch is the dominant non-linearity; careful layout and calibration are needed for production-grade INL/DNL

## Repository

Source on [GitHub](https://github.com/devesh-b/4bit-Flash-ADC).
