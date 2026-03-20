# Jeremie Louvaert

**Founder @ [AKURATE.STUDIO](https://akurate.studio)** — Building tools at the intersection of generative AI and production workflows.

---

## What I Build

I create **open-source custom nodes for ComfyUI** — the leading node-based interface for Stable Diffusion and AI image/video generation. My focus is solving real production pain points: API cost management, conversational image editing, workflow organization, and prompt engineering tooling.

---

## Open Source Projects

### [ComfyUI-Gemini-Conversation-Canvas](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Conversation-Canvas) 🆕

Multi-turn conversational image editing powered by Google Gemini's native image generation.

- **Session Start** — Create a conversation and generate an initial image from text or image input
- **Edit Turn** — Chain natural language edits with full scene coherence across turns
- **Session Persistence** — Save and resume conversations across ComfyUI restarts
- **Session Gallery** — View all turn images side by side for visual comparison
- The only ComfyUI node suite that leverages Gemini's multi-turn conversation memory for image editing

### [ComfyUI-API-Optimizer](https://github.com/jeremieLouvaert/ComfyUI-API-Optimizer)

Production-grade custom nodes for optimizing external API workflows in ComfyUI.

- **API Cost & Quota Tracker** — Circuit-breaker for cloud API spending with persistent ledger and audit logging
- **Deterministic Hash Vault** — Aggressive disk-caching layer that hashes prompts, parameters, and tensors
- **Lazy API Switch** — Physically prevents upstream API node execution on cache hits, saving money and time
- Supports cloud providers: Kling, Magnific, Banana.dev, RunPod, and any REST API

### [comfyui-prompt-assembler](https://github.com/jeremieLouvaert/comfyui-prompt-assembler)

Modular prompt assembly nodes with per-slot ON/OFF toggles.

- **Standard (8 slots)** — Full-featured with debug output and configurable separators
- **Compact (4 slots)** — Lightweight version for simple workflows
- **Weighted (6 slots)** — Attention weight control with automatic `(prompt:weight)` syntax

### [comfyui-wireless-link-simple](https://github.com/jeremieLouvaert/comfyui-wireless-link-simple)

Wireless data transmission nodes inspired by Blackmagic Fusion.

- Send and Get any ComfyUI data type without visible wire connections
- Named channels for clear, organized workflows
- Works with IMAGE, MODEL, LATENT, CLIP, VAE, and all other types

---

## Technical Focus

| Area | Details |
|------|--------|
| **ComfyUI Custom Nodes** | Python-based node authoring for AI generation pipelines |
| **Conversational Image Editing** | Multi-turn Gemini conversations with session persistence |
| **API Cost Optimization** | Circuit-breaker patterns, budget enforcement, deterministic caching |
| **Workflow Architecture** | Tools that make complex AI pipelines manageable and production-ready |
| **Generative AI Tooling** | Stable Diffusion, SDXL, Flux, Gemini, image generation, video generation |
| **Prompt Engineering** | Modular prompt construction, attention weighting, template systems |

---

## Tech Stack

`Python` `PyTorch` `ComfyUI` `Google Gemini API` `TypeScript` `Node.js` `REST APIs` `Git`

---

## About AKURATE.STUDIO

[AKURATE.STUDIO](https://akurate.studio) is a premium brand intelligence platform combining AI-driven analysis with creative production tools.

---

## Connect

- **Website:** [akurate.studio](https://akurate.studio)
- **GitHub:** [@jeremieLouvaert](https://github.com/jeremieLouvaert)
- **Email:** jeremie.louvaert@gmail.com
