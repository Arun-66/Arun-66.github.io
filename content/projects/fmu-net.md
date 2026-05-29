---
layout: project
title: "FMU-NET: Semantic Segmentation for Person ID"
description: "Novel semantic segmentation architecture for person identification. Published at EASCT 2023."
category: "Software & ML"
tags: [PyTorch, Computer Vision, Segmentation, Deep Learning]
doi: "10.1109/EASCT59475.2023.10392590"
---

## Overview

FMU-NET is a semantic segmentation architecture designed specifically for person identification in challenging scenes — partial occlusion, crowded backgrounds, and variable lighting. The model produces dense per-pixel labels separating person instances from background, which a downstream re-identification module then uses for matching.

## Architecture

The network uses an encoder-decoder backbone with multi-scale feature fusion. Key design decisions:

- **Feature pyramid neck**: captures fine-grained silhouette detail at high resolution while retaining semantic context from deeper feature maps
- **Attention gates**: suppress irrelevant background activations before skip connections, improving precision at person boundaries
- **Lightweight decoder**: designed for inference efficiency relative to segmentation models with heavier decoders

## Results

Evaluated on standard person re-identification benchmarks. The segmentation pre-processing step improves downstream re-ID accuracy by reducing background noise in the feature space.

## Publication

Published at **IEEE EASCT 2023** (Emerging Applications of Signal, Communication, and Technology).
