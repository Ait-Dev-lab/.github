# 🧠 Ait-Dev-lab

**Research lab focused on browser-native AI inference.**

We build LLM infrastructure that runs entirely on user devices — **no API keys, no cloud GPUs, no rate limits.**

---

## 🎯 Mission

Democratize AI by making large language models run **locally in the browser** — private, free, and accessible to anyone with a modern device.

---

## 🔬 Research Areas

| Area | Focus |
|------|-------|
| **WebGPU Inference** | Compute shaders for LLM acceleration |
| **Model Sharding** | Splitting large models into browser-friendly chunks |
| **Memory Optimization** | Running on 256MB-512MB integrated GPUs |
| **Streaming Architecture** | Hybrid server/client token generation |

---

## 📦 Current Projects

| Project | Description |
|---------|-------------|
| [Stream LLM](https://github.com/Ait-Dev-lab/stream-llm) | Browser-based LLM inference with on-demand shard fetching |

---

## ⚡ Technical Approach

| Challenge | Our Solution |
|-----------|--------------|
| Expensive GPUs | Consumer integrated GPU support (256MB+) |
| API costs | No keys, no payments |
| Privacy | Local browser processing |
| Large models | 30+ shards, fetched on demand |
| Cold starts | Jumpstart server + uptime monitoring |

---

## 🛠️ Stack

- **WebGPU** — Compute shaders
- **GGUF Sharding** — Model splitting
- **GitHub Releases** — Free CDN
- **Render** — Jumpstart API
- **GitHub Pages** — Hosting

---

## 🚀 Live Demo

**👉 [Try Stream LLM](https://ait-dev-lab.github.io/stream-llm/) 👈**

Requires Chrome 113+ or Edge 113+

---

## 📄 License

MIT © Ait-Dev-lab

---

*Building the infrastructure for browser-native AI.*