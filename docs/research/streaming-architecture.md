---
title: Streaming Architecture for LLM Inference
description: Hybrid server/client token generation for instant responses
date: 2026-05-15
category: Research
status: Ongoing
---

# Streaming Architecture for LLM Inference

## Overview

Our hybrid architecture combines a lightweight jumpstart server with client-side WebGPU processing.

## How It Works

1. User submits prompt in browser
2. Jumpstart server generates first 8 tokens (instant)
3. Browser fetches model shards from CDN
4. WebGPU processes remaining layers
5. Tokens stream to user in real-time

## Jumpstart Server

A lightweight Express server on Render free tier that:
- Generates first 8 tokens immediately
- Returns model configuration
- Provides uptime monitoring via UptimeRobot

## Client-Side Processing

After jumpstart, the browser:
- Fetches shards from CDN
- Uploads weights to GPU
- Executes compute shaders
- Streams tokens to output

## Latency Breakdown

| Step | Time |
|------|------|
| Jumpstart | ~200-500ms |
| Per shard fetch | ~100-300ms |
| GPU processing | ~50-100ms per layer |

## Current Status

- Jumpstart server: Routes partially implemented
- CDN shards: Complete (30 shards, 1.87GB)
- Client streaming: Token generation working

## Next Steps

- Complete jumpstart API routes
- Optimize shader performance
- Implement token streaming smoothing
