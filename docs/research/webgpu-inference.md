---
title: WebGPU Inference for LLMs
description: How we use compute shaders to run large language models directly in the browser
date: 2026-05-15
category: Research
status: Active
---

# WebGPU Inference for LLMs

## Overview

We leverage WebGPU compute shaders to run LLM inference entirely in the browser, eliminating the need for cloud GPUs or API keys.

## Key Achievements

- Successfully running Llama-3.2-3B in Chrome/Edge
- 512MB buffer size working on T4 GPUs
- Device capability detection with graceful fallbacks
- 30-shard model splitting for on-demand loading

## Technical Implementation

### GPU Adapter Request

const adapter = await navigator.gpu.requestAdapter();
const device = await adapter.requestDevice({
    requiredLimits: {
        maxStorageBufferBindingSize: 512 * 1024 * 1024
    }
});

### Compute Shader Pattern

The shader reads weights and tokens, processes them in parallel, and outputs logits for token selection.

## Results

Initial tests show successful inference at ~10-15 tokens per second on a T4 GPU.

## Next Steps

- Optimize shader performance
- Reduce memory footprint
- Add support for smaller models on 256MB GPUs
