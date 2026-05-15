---
title: Memory Optimization for Consumer GPUs
description: Running LLMs on 256MB-512MB integrated GPUs
date: 2026-05-15
category: Research
status: Ongoing
---

# Memory Optimization for Consumer GPUs

## The Challenge

Most consumer GPUs have limited buffer sizes (128MB-512MB), far less than the 2GB+ typically required for LLMs.

## Our Solution

### Device Detection

We check GPU capabilities before requesting the device:

- 1024MB+ → Full model
- 512MB → Full model
- 256MB → Needs smaller model
- 128MB → Not supported

### Sharded Loading

Instead of loading the entire model, we load one shard at a time and evict from memory after processing.

## GPU Tier Support

| Tier | Buffer | Support |
|------|--------|---------|
| High-end discrete | 1024MB+ | Full model |
| Mid-range discrete | 512MB | Full model |
| Integrated modern | 256MB | Partial (in progress) |
| Integrated older | 128MB | None |

## Next Steps

- Create 256MB-compatible model variant
- Quantize to 3-bit or 2-bit
- Explore layer skipping techniques
