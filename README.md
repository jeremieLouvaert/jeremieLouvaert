# Jeremie Louvaert

**Founder @ [AKURATE.STUDIO](https://jeremielouvaert.com)** — Building tools at the intersection of generative AI and production workflows.

---

## What I Build

I create **7 open-source custom node packs for ComfyUI** (50+ nodes total) — the leading node-based interface for Stable Diffusion and AI image/video generation. My focus is professional color grading, direct API integrations, conversational image editing, cost optimization, prompt engineering, and workflow organization.

---

## Open Source Projects

### [ComfyUI-Darkroom](https://github.com/jeremieLouvaert/ComfyUI-Darkroom)

Professional color grading & film emulation suite for ComfyUI. 29 nodes across four modules:

**Film Emulation (6 nodes)** — 161 film stocks (111 color + 50 B&W) with real Capture One curve data parsed from 586 .costyle XML files. Film Grain, Halation, Print Stock, Cross Process.

**Camera Raw (9 nodes)** — White Balance, Exposure & Tone, HSL Selective, Clarity/Texture/Dehaze, Vibrance, Sharpening Pro, Noise Reduction, Skin Tone Uniformity, Color Qualifier.

**Color Grading (9 nodes)** — Tone Curve (cubic spline), Lift Gamma Gain (Resolve primary corrector), Log Wheels (log2-space zone grading), 3-Way Color Balance (15 creative presets), Hue vs Hue, Hue vs Sat, Lum vs Sat, Sat vs Sat, Color Warper.

**Lens & Optics (5 nodes)** — Chromatic Aberration, Vignette, Lens Distortion, Perspective Correct, Lens Profile with 102 real lens models across 10 brands.

- Physics-based: H&D characteristic curves, cos^4 vignette law, Brown-Conrady distortion, PchipInterpolator tone curves
- 75+ grading presets across all nodes
- Zero API costs — pure local computation

### [ComfyUI-Gemini-Direct](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Direct)

Direct Google Gemini image generation for ComfyUI. Bypass credits, use your own API key.

- **Gemini Image Generate** — Direct API call supporting Gemini 2.0 Flash, 2.5 Flash, and 2.5 Pro models
- **Prompt Studio (AI Enhancer)** — Domain-adaptive prompt expansion and refinement with anti-AI realism mandate
- USD cost display per generation, cache key output for Hash Vault compatibility
- Drop-in replacement for credit-based Gemini wrappers

### [ComfyUI-Gemini-Conversation-Canvas](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Conversation-Canvas)

Multi-turn conversational image editing powered by Google Gemini’s native image generation.

- **Session Start** — Create a conversation and generate an initial image from text or image input
- **Edit Turn** — Chain natural language edits with full scene coherence across turns
- **Session Persistence** — Save and resume conversations across ComfyUI restarts
- **Session Gallery** — View all turn images side by side for visual comparison
- The only ComfyUI node suite that leverages Gemini’s multi-turn conversation memory for image editing

### [ComfyUI-Higgsfield-Direct](https://github.com/jeremieLouvaert/ComfyUI-Higgsfield-Direct)

Direct Higgsfield API integration — multi-model image & video generation.

- **Higgsfield Text-to-Image** — Soul 2.0, Seedream 4, Reve models with resolution/aspect control
- **Higgsfield Image Edit** — Seedream 4 Edit for text-guided image editing
- **Higgsfield Image-to-Video** — Kling 2.1 Pro, Seedance Pro, DOP Preview with 5/10/15s durations
- **Higgsfield Model Info** — Utility node listing available models and capabilities

### [ComfyUI-API-Optimizer](https://github.com/jeremieLouvaert/ComfyUI-API-Optimizer)

Production-grade custom nodes for optimizing external API workflows in ComfyUI.

- **API Cost & Quota Tracker** — Circuit-breaker for cloud API spending with persistent ledger and audit logging
- **Deterministic Hash Vault** — Aggressive disk-caching layer that hashes prompts, parameters, and tensors
- **Lazy API Switch** — Physically prevents upstream API node execution on cache hits, saving money and time
- Supports cloud providers: Kling, Magnific, Banana.dev, RunPod, and any REST API

### [ComfyUI-Prompt-Vault](https://github.com/jeremieLouvaert/ComfyUI-Prompt-Vault)

Photographic prompt arsenal — curated exclusively for photorealism.

- **Prompt Vault Browse** — 21 curated elite templates across 8 categories, filtered from 12,000+ raw prompts
- **Prompt Vault Build** — Assemble prompts from 100+ components: 27 cameras, 24 lighting setups, 18 film stocks, 15 moods
- **Prompt Vault Favorites** — Persistent prompt library across sessions
- Zero dependencies, zero API costs

### [comfyui-wireless-link-simple](https://github.com/jeremieLouvaert/comfyui-wireless-link-simple)

Wireless data transmission nodes inspired by Blackmagic Fusion.

- Send and Get any ComfyUI data type without visible wire connections
- Named channels for clear, organized workflows
- Works with IMAGE, MODEL, LATENT, CLIP, VAE, and all other types

---

## Technical Focus

| Area | Details |
|------|--------|
| **Professional Color Grading** | 29-node suite: physics-based film emulation, Resolve-level grading, Camera Raw tools, lens optics. 161 stocks, 102 lenses, 75+ presets |
| **ComfyUI Custom Nodes** | Python-based node authoring for AI generation pipelines |
| **Conversational Image Editing** | Multi-turn Gemini conversations with session persistence |
| **API Cost Optimization** | Circuit-breaker patterns, budget enforcement, deterministic caching |
| **Workflow Architecture** | Tools that make complex AI pipelines manageable and production-ready |
| **Generative AI Tooling** | Stable Diffusion, SDXL, Flux, Gemini, Higgsfield, image/video generation |
| **Prompt Engineering** | Modular prompt construction, photorealism components, template systems |

---

## Tech Stack

`Python` `PyTorch` `ComfyUI` `Google Gemini API` `Higgsfield API` `scipy` `numpy` `TypeScript` `Node.js` `REST APIs` `Git`

---

## About AKURATE.STUDIO

[AKURATE.STUDIO](https://jeremielouvaert.com) is a premium brand intelligence platform combining AI-driven analysis with creative production tools.

---

## Connect

- **Website:** [jeremielouvaert.com](https://jeremielouvaert.com)
- **GitHub:** [@jeremieLouvaert](https://github.com/jeremieLouvaert)
- **Email:** jeremie.louvaert@gmail.com
