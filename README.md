# Awesome Uncensored AI Image Models

> A community-maintained catalog of current AI image-generation and image-editing models—including local weights, hosted products, and APIs—with a focus on filtering, access, and practical trade-offs.

"Uncensored" is not a standardized technical term. A model's behavior can change with the checkpoint, prompt wrapper, inference UI, safety checker, provider policy, and version. This list records those details instead of treating the label as a guarantee.

**Last reviewed:** 2026-08-05

## Contents

- [Recent catalog](#recent-catalog)
- [Community-labeled uncensored variants](#community-labeled-uncensored-variants)
- [Established local baselines](#established-local-baselines)
- [Community checkpoints and fine-tunes](#community-checkpoints-and-fine-tunes)
- [How entries are classified](#how-entries-are-classified)
- [What each entry should include](#what-each-entry-should-include)
- [Contributing](#contributing)
- [Responsible use](#responsible-use)

## Recent catalog

This section includes both open-weight and proprietary/hosted models. Hosted models are listed for comparison and are subject to the provider's terms and safety systems; they should not be described as uncensored merely because they are accessible through an API.

### 2026 releases and current models

| Model | Release / update | Access | Best known for | Filtering / policy | Official source |
| --- | --- | --- | --- | --- | --- |
| GPT Image 2 / ChatGPT Images 2.0 | 2026-04-21 | Hosted / API | General generation, editing, typography, and visual reasoning | Provider policy and safety systems | [API model](https://developers.openai.com/api/docs/models/gpt-image-2) · [announcement](https://openai.com/index/introducing-chatgpt-images-2-0/) |
| Gemini 3.1 Flash Image (Nano Banana 2) | 2026 | Hosted / API | Fast generation, multi-turn editing, references, and 4K output | Google policy; SynthID watermarking | [Gemini image guide](https://ai.google.dev/gemini-api/docs/image-generation) |
| Gemini 3 Pro Image (Nano Banana Pro) | 2026 | Hosted / API | Complex visual tasks, grounding, and high-fidelity editing | Google policy; SynthID watermarking | [Gemini image guide](https://ai.google.dev/gemini-api/docs/image-generation) |
| Recraft V4.1 family | 2026-05-30 | Hosted / API | Design direction, production graphics, utility layouts, and vectors | Provider policy; hosted only | [Release](https://www.recraft.ai/press-releases/recraft-v4-1-utility-pro-becomes-the-highest-ranked-text-to-image-model-outside-google-and-openai) |
| Ideogram 4.0 | 2026-06-03 | Open weights / API | Typography, layout control, brand assets, and 2K images | Verify the model card and deployment pipeline | [Release](https://ideogram.ai/news/ideogram-4.0/) · [technical details](https://ideogram.ai/blog/ideogram-4.0/) |
| HiDream-O1-Image / Dev-2604 | 2026-05 | Local weights | Text-to-image, editing, personalization, and long text layout | To verify per checkpoint and pipeline | [Model card](https://huggingface.co/HiDream-ai/HiDream-O1-Image) |
| Seedream 5.0 Lite | 2026-02-13 | Hosted / API | Multimodal generation, editing, reasoning, and current-information visuals | Provider policy; hosted only | [Official release](https://seed.bytedance.com/en/blog/deeper-thinking-more-accurate-generation-introducing-seedream-5-0-lite) |
| Qwen-Image-2.0 | 2026-02-10 | Hosted / API | Professional typography, 2K generation, and unified editing | Hosted policy; availability and terms vary | [Official project](https://github.com/QwenLM/Qwen-Image) |
| HunyuanImage-3.0-Instruct / Distil | 2026-01-26 | Local weights | Prompt reasoning, image-to-image editing, and efficient inference | To verify per checkpoint and pipeline | [Official project](https://github.com/Tencent-Hunyuan/HunyuanImage-3.0) |
| FLUX.2 [klein] 4B / 9B | 2026-01-15 | Local weights / API | Fast generation and editing on consumer hardware | 4B is Apache-2.0; 9B has FLUX terms; local pipeline-dependent | [Official inference repo](https://github.com/black-forest-labs/flux2) |

### 2025 releases still worth tracking

| Model | Release / update | Access | Best known for | Filtering / policy | Official source |
| --- | --- | --- | --- | --- | --- |
| GPT Image 1.5 | 2025-12-16 | Hosted / API | Precise editing, image preservation, and dense text | Provider policy and safety systems | [Announcement](https://openai.com/index/new-chatgpt-images-is-here/) |
| Qwen-Image-2512 / Edit-2511 / Layered | 2025-12 | Local weights | Realism, editing consistency, and layer decomposition | To verify per checkpoint and pipeline | [Official project](https://github.com/QwenLM/Qwen-Image) · [model collection](https://huggingface.co/collections/Qwen/qwen-image) |
| FLUX.2 [pro] / [flex] / [max] | 2025-11-25 onward | Hosted / API | Production generation, editing, typography, and control | Provider policy; API terms apply | [Release notes](https://docs.bfl.ai/release-notes) |
| FLUX.2 [dev] | 2025-11-25 | Local weights | High-quality text-to-image and single/multi-reference editing | FLUX non-commercial terms; inference filters/manual review required by the license | [Model card](https://huggingface.co/black-forest-labs/FLUX.2-dev) |
| Adobe Firefly Image Model 5 | 2025-10-28 | Hosted | Commercial creative workflows and photorealism | Adobe's commercially safe model and provider controls | [Adobe announcement](https://news.adobe.com/news/2025/10/adobe-max-2025-firefly) |
| Seedream 4.5 | 2025 | Hosted / API | Multi-image editing, reference consistency, and typography | Provider policy; hosted only | [Official model page](https://seed.bytedance.com/en/seedream4_5) |
| Seedream 4.0 | 2025-09-09 | Hosted / API | Unified generation/editing and up to 4K output | Provider policy; hosted only | [Official release](https://seed.bytedance.com/en/blog/seedream-4-0-officially-released-beyond-drawing-into-imagination) |
| Nano Banana (Gemini 2.5 Flash Image) | 2025 | Hosted / API | Fast conversational image generation and editing | Google policy; SynthID watermarking | [Model page](https://ai.google.dev/gemini-api/docs/models/gemini-2.5-flash-image) |
| Imagen 4 | 2025-05-20 | Hosted / API | Photorealism, styles, detail, text, and up to 2K output | Google policy; migration path should be checked | [Google DeepMind](https://deepmind.google/models/imagen/) |
| Midjourney V7 | 2025-04-30 update | Hosted | Aesthetics, prompt accuracy, and coherent subjects | Hosted moderation and platform policy | [Official update](https://updates.midjourney.com/v7-update-editor-and-exp/) |
| Ideogram 3.0 | 2025-03-26 | Hosted / API | Text rendering, graphic design, and style references | Hosted moderation and platform policy | [Official release](https://about.ideogram.ai/3.0) |

## Community-labeled uncensored variants

Recent model cards and community checkpoints use “uncensored” in several different ways: a modified text encoder, an adult-content fine-tune, removal of an optional safety component, or simply a repository name. The [dedicated uncensored-variants catalog](UNCENSORED-MODELS.md) records the evidence, base model, access requirements, and licensing caveats for each entry.

The strongest recent examples found during the 2026-08-05 review are FLUX.2 Klein uncensored text-encoder variants, a Qwen-Image NSFW LoRA, and FLUX.1/SDXL community checkpoints. These are community claims unless the entry is explicitly marked otherwise; local execution does not remove legal or license restrictions.

## Established local baselines

These are established local models that remain useful reference points. Their presence here is not a claim that they are uncensored; verify the exact version, license, and inference pipeline before using or classifying them.

### General-purpose and research models

| Model | Access | Family | Filtering status | Source |
| --- | --- | --- | --- | --- |
| FLUX.1 [dev] | Local weights | FLUX | To verify | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-dev) |
| Stable Diffusion XL Base 1.0 | Local weights | SDXL | To verify | [Model card](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0) |
| Stable Diffusion v1.5 | Local weights | Stable Diffusion | To verify | [Model card](https://huggingface.co/runwayml/stable-diffusion-v1-5) |
| PixArt-Σ | Local weights | PixArt | To verify | [Model card](https://huggingface.co/PixArt-alpha/PixArt-Sigma-XL-2-1024-MS) |
| Playground v2.5 | Local weights | Playground | To verify | [Model card](https://huggingface.co/playgroundai/playground-v2.5-1024px-aesthetic) |

### Community checkpoints and fine-tunes

| Model | Access | Focus | Filtering status | Source |
| --- | --- | --- | --- | --- |
| DreamShaper XL 1.0 | Local weights | General / stylized | To verify | [Model card](https://huggingface.co/Lykon/dreamshaper-xl-1-0) |
| Animagine XL 3.1 | Local weights | Anime / illustration | To verify | [Model card](https://huggingface.co/cagliostrolab/animagine-xl-3.1) |

Want to add a model? Use the [submission template](.github/ISSUE_TEMPLATE/model-submission.md) or open a pull request.

## How entries are classified

- **Verified low-filter** — the exact checkpoint and inference setup are documented, and a maintainer has reproduced the reported behavior.
- **Community-reported** — a contributor has supplied reproducible details, but a maintainer has not independently checked them yet.
- **Provider-filtered** — hosted access is governed by a provider's content policy and safety systems; local uncensored behavior cannot be inferred.
- **To verify** — the model is a useful catalog candidate, but its filtering behavior or licensing details still need documentation.
- **Removed** — the source is unavailable, the license is unclear, or the entry repeatedly fails the contribution requirements.

These labels describe observed behavior and documentation quality. They do not grant permission to create, distribute, or use any particular content.

## What each entry should include

Every accepted entry should document:

- exact model and checkpoint version;
- release date or most recent major update;
- official source, access method, and download/API links;
- whether it is local, hosted, API-only, or available in multiple forms;
- base architecture and intended use;
- license, commercial-use terms, provider terms, and restrictions;
- approximate VRAM, latency, or hardware requirements where known;
- supported inference tools or workflows;
- whether filtering is in the weights, the pipeline, the UI, the provider, or an optional safety checker;
- reproducible notes about testing, including date and setup.

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a model. Short version: cite primary sources, preserve license and provider terms, avoid vague “uncensored” claims, and keep entries factual and reproducible.

## Responsible use

Use these resources for lawful, consensual, and ethical creative or research work. Do not use them to create sexual content involving minors, non-consensual intimate imagery, targeted harassment, fraud, impersonation, or other abusive or illegal material. Follow the model license, provider terms, and the laws that apply to you.

## License

The original documentation and catalog content in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Individual models, providers, APIs, checkpoints, and linked resources remain subject to their own licenses and terms.
