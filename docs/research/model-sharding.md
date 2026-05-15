---
title: Model Sharding for Browser LLMs
description: Splitting 2GB+ models into 30+ small chunks for on-demand loading
date: 2026-05-15
category: Research
status: Complete
---

# Model Sharding for Browser LLMs

## Overview

We split large language models into small, independently loadable shards that the browser fetches on demand.

## Shard Statistics

| Metric | Value |
|--------|-------|
| Total shards | 30 |
| Total size | 1.87 GB |
| Largest shard | 308 MB |
| Average shard | 55 MB |

## CDN Architecture

Shards are hosted on GitHub Releases, providing free CDN with worldwide distribution.

`https://github.com/Ait-Dev-lab/stream-llm/releases/download/v1.0.0/shard_XXX.bin`

## Benefits

- On-demand fetching reduces initial load time
- Browser caching per shard
- No server costs
- Works offline after download
