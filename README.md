# Jeremie Louvaert

**Jeremie Louvaert is a software developer, senior CG artist and photographer based in Sint-Denijs, Belgium. He builds open-source custom nodes for ComfyUI in Python: colour grading and film emulation, procedural fields and data art, direct API integrations for Gemini, OpenAI GPT Image, Higgsfield and Midjourney, and workflow tools. Founder of AKURATE.STUDIO.**

[![Website](https://img.shields.io/badge/jeremielouvaert.com-website-blue)](https://jeremielouvaert.com) [![GitHub](https://img.shields.io/badge/jeremieLouvaert-GitHub-black)](https://github.com/jeremieLouvaert)

## What I build

14 open-source packs for [ComfyUI](https://github.com/comfyanonymous/ComfyUI), the node-based interface for AI image and video generation: 108 nodes in 12 packs, plus 2 frontend extensions. All of them are on the Comfy Registry and install from ComfyUI Manager.

| Pack | Nodes | What it does |
|------|------:|--------------|
| [ComfyUI-Darkroom](https://github.com/jeremieLouvaert/ComfyUI-Darkroom) | 59 | Colour grading, film emulation, RAW, scopes, CMYK print and LUT export |
| [ComfyUI-Field](https://github.com/jeremieLouvaert/ComfyUI-Field) | 15 | Resolution-independent procedural masks for driving effects |
| [ComfyUI-Schematic](https://github.com/jeremieLouvaert/ComfyUI-Schematic) | 4 | Technical data-art overlays, construction plates, Voronoi and topographic sheets |
| [ComfyUI-Gemini-Direct](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Direct) | 6 | Gemini image and video generation on your own API key |
| [ComfyUI-Gemini-Conversation-Canvas](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Conversation-Canvas) | 5 | Multi-turn image editing as a saved Gemini conversation |
| [ComfyUI-GPT-Image-Direct](https://github.com/jeremieLouvaert/ComfyUI-GPT-Image-Direct) | 1 | OpenAI GPT Image 2.6 on your own API key, with exact cost per run |
| [ComfyUI-Higgsfield-Direct](https://github.com/jeremieLouvaert/ComfyUI-Higgsfield-Direct) | 4 | Higgsfield text-to-image, image edit and image-to-video |
| [ComfyUI-Midjourney-Direct](https://github.com/jeremieLouvaert/ComfyUI-Midjourney-Direct) | 1 | Midjourney in ComfyUI through LegNext.ai, no Discord |
| [ComfyUI-API-Optimizer](https://github.com/jeremieLouvaert/ComfyUI-API-Optimizer) | 5 | Budget tracking and hash caching for paid API calls |
| [ComfyUI-Prompt-Vault](https://github.com/jeremieLouvaert/ComfyUI-Prompt-Vault) | 3 | Photographic prompt templates and a component builder |
| [comfyui-prompt-assembler](https://github.com/jeremieLouvaert/comfyui-prompt-assembler) | 3 | Join prompt fragments with per-slot toggles and weights |
| [comfyui-wireless-link-simple](https://github.com/jeremieLouvaert/comfyui-wireless-link-simple) | 2 | Send and get any data type without a wire |
| [ComfyUI-ReferenceCopy](https://github.com/jeremieLouvaert/ComfyUI-ReferenceCopy) | frontend | Houdini-style live-linked node clones |
| [ComfyUI-EphemeralPeek](https://github.com/jeremieLouvaert/ComfyUI-EphemeralPeek) | frontend | Alt+click an output socket to preview it, no preview node |

## Image finishing

### [ComfyUI-Darkroom](https://github.com/jeremieLouvaert/ComfyUI-Darkroom)

A colour grading and film emulation suite that runs locally, with no API cost. 59 nodes, 161 film stocks (111 colour, 50 B&W), 35 spectral negative-by-print LUTs and 102 lens profiles.

- Film emulation (14 nodes): film stocks, Film Grain Pro (resolution-independent stochastic grain after Newson et al. 2017), annular halation, print stock, cross process, Sabattier, reciprocity failure, light leaks, film damage and rebate borders.
- Camera Raw and colour grading (20 nodes): white balance, HSL, tone curve, lift/gamma/gain, log wheels, 3-way balance, hue and saturation curves.
- Lens and optics (7 nodes), including long-exposure camera shake and water refraction through exact Snell's law.
- RAW pipeline with rawpy/LibRaw and Adobe .dcp profiles, histogram and vectorscope, reference colour match, CMYK TIFF export with an embedded ICC profile, and halftone.
- LUT export to .cube, colour space transforms (sRGB, ACEScg, ACEScct, Rec.2020, DCI-P3) and ACES/AgX tonemapping. Grade in ComfyUI, finish in Resolve or Photoshop.
- Since 1.28.0, 24 nodes run their whole pipeline on the GPU, typically 15 to 80 times faster.

## Procedural fields and data art

### [ComfyUI-Field](https://github.com/jeremieLouvaert/ComfyUI-Field)

Resolution-independent masks for driving and masking effects. A 512 px preview and a 4K render show the same picture.

- Generate: Perlin, simplex, value and Worley noise, analytic gradients with a stops-ramp editor, shapes, tiles and scatter.
- Shape and refine: remap, threshold, distance, morphology, warp.
- Derive masks from an image, its edges (Sobel, Scharr, Laplacian, hysteresis) or its detail. Field Composite then varies any effect across the frame.
- `coverage` is made exact with a probability integral transform, so a noise mask covers the share of the frame you ask for.

### [ComfyUI-Schematic](https://github.com/jeremieLouvaert/ComfyUI-Schematic)

Technical data-art nodes.

- Schematic Overlay: detection circles, tangent chains, crosshair frames and pixelation zones over a photo.
- Schematic Construction: projective-geometry plates with ray pencils, concentric spheres and computed intersections.
- Schematic Voronoi: the photo becomes the density field of a 12,000-cell tessellation.
- Schematic Topographic: seeded procedural map sheets with contours, hachures, spot heights and marginalia.

## Generation on your own API key

These packs call the provider directly with your key, show the real USD cost of each run, and output a `cache_key` for the API Optimizer's Hash Vault.

### [ComfyUI-Gemini-Direct](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Direct)

- Gemini Image Generate: Gemini 3 Pro Image (Nano Banana Pro), Nano Banana 2.1, Gemini 3.1 Flash Image and 2.5 Flash Image, up to 4K.
- Gemini Video Omni: 3 to 10 second 720p clips with audio, up to 14 reference images, and conversational edits chained by `interaction_id`. About $0.10 per second.
- Gemini Style Transfer: 23 photographer styles applied to your image.
- Prompt Studio: expands, refines and edits prompts on Gemini 3 Flash for about $0.001 a call.

### [ComfyUI-Gemini-Conversation-Canvas](https://github.com/jeremieLouvaert/ComfyUI-Gemini-Conversation-Canvas)

Multi-turn image editing. Each edit is a new turn in a Gemini conversation, so the model remembers the scene. Sessions save to disk and reload after a restart, and a gallery node shows every turn side by side.

### [ComfyUI-GPT-Image-Direct](https://github.com/jeremieLouvaert/ComfyUI-GPT-Image-Direct)

One node for OpenAI GPT Image 2.6 Flare and Sunburst, plus 2.5, 2, 1.5 and 1-mini.

- Text-to-image, or edits from up to 16 reference images with an optional inpaint mask.
- On 2.6: animated GIF output, SVG output, markup-guided edits and a complexity setting.
- Exact USD cost per run from the API's own token counts.

### [ComfyUI-Higgsfield-Direct](https://github.com/jeremieLouvaert/ComfyUI-Higgsfield-Direct)

Higgsfield text-to-image (Soul 2.0, Seedream 4, Reve), image edit (Seedream 4 Edit) and image-to-video (Kling 2.1 Pro, Seedance Pro, DOP), with 5, 10 or 15 second clips as native ComfyUI VIDEO.

### [ComfyUI-Midjourney-Direct](https://github.com/jeremieLouvaert/ComfyUI-Midjourney-Direct)

Midjourney has no official public API, so this node goes through the LegNext.ai proxy. No Discord. v7 by default, plus v6.1, v6 and niji 6, with stylize, weird, chaos and the other flags as real inputs.

## Workflow tools

### [ComfyUI-API-Optimizer](https://github.com/jeremieLouvaert/ComfyUI-API-Optimizer)

Stops paid API calls you don't need. The cost tracker keeps a persistent ledger and halts the run before it goes over budget. The Hash Vault hashes the prompt, parameters and input tensors, and on a cache hit the Lazy API Switch never runs the API node at all. A browser gallery (Ctrl+Shift+H) shows everything in the vault.

### [ComfyUI-Prompt-Vault](https://github.com/jeremieLouvaert/ComfyUI-Prompt-Vault)

Photographic prompts only: 21 curated templates and a builder with 101 components (27 camera and lens setups, 24 lighting setups, 18 film stocks, 15 moods), plus a favourites list that persists between sessions.

### [comfyui-prompt-assembler](https://github.com/jeremieLouvaert/comfyui-prompt-assembler)

Joins prompt fragments with an on/off toggle per slot. The weighted version wraps each fragment in `(text:1.30)` attention syntax.

### [comfyui-wireless-link-simple](https://github.com/jeremieLouvaert/comfyui-wireless-link-simple)

Send any data type on a named channel and get it back elsewhere in the graph without a wire. Inspired by Blackmagic Fusion's wireless link.

### [ComfyUI-ReferenceCopy](https://github.com/jeremieLouvaert/ComfyUI-ReferenceCopy)

Houdini-style reference copies. Ctrl+Alt+C clones a node and keeps every parameter live-linked to the original. Change one parameter on the copy and only that one unlinks. The links are saved in the workflow.

### [ComfyUI-EphemeralPeek](https://github.com/jeremieLouvaert/ComfyUI-EphemeralPeek)

Alt+click any output socket for a floating preview of that output. It runs only the part of the graph that preview needs and never touches the saved workflow.

## Tech stack

`Python` `PyTorch` `NumPy` `SciPy` `ComfyUI` `JavaScript` `LiteGraph` `Google Gemini API` `OpenAI API` `Higgsfield API` `rawpy/LibRaw` `TypeScript` `Node.js` `Git`

## About AKURATE.STUDIO

[AKURATE.STUDIO](https://jeremielouvaert.com) is the umbrella name we develop our creative tools under, these ComfyUI packs included.

## Connect

- Website: [jeremielouvaert.com](https://jeremielouvaert.com)
- GitHub: [@jeremieLouvaert](https://github.com/jeremieLouvaert)
- Email: jeremie.louvaert@gmail.com
