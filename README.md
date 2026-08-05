# Awesome Uncensored AI Image Models

> A community-maintained catalog of current AI image-generation and image-editing models—including local weights, hosted products, and APIs—with a focus on filtering, access, and practical trade-offs.

"Uncensored" is not a standardized technical term. A model's behavior can change with the checkpoint, prompt wrapper, inference UI, safety checker, provider policy, and version. This list records those details instead of treating the label as a guarantee.

**Last reviewed:** 2026-08-06

## Related Projects

- [awesome-ai-image-models](https://github.com/Anil-matcha/awesome-ai-image-models) — Compare mainstream and open image models by provider, price, and capability alongside this filtering-focused catalog.
- [awesome-uncensored-ai-video-models](https://github.com/Anil-matcha/awesome-uncensored-ai-video-models) — Companion catalog for video-generation and video-editing model variants.
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — Self-hosted image and video studio for testing generative-media workflows.
- [Generative-Media-Skills](https://github.com/SamurAIGPT/Generative-Media-Skills) — Run and automate media-generation experiments from an AI coding agent.

## Contents

- [Recent catalog](#recent-catalog)
- [Filtered reference models](#filtered-reference-models)
- [Community-reported uncensored variants](#community-reported-uncensored-variants)
- [Established local baselines](#established-local-baselines)
- [Community checkpoints and fine-tunes](#community-checkpoints-and-fine-tunes)
- [How entries are classified](#how-entries-are-classified)
- [What each entry should include](#what-each-entry-should-include)
- [Contributing](#contributing)
- [Responsible use](#responsible-use)

## Recent catalog

The recent catalog includes local open-weight models and community-reported uncensored or low-filter hosted endpoints. Access method and provider still matter: the same model family can behave differently across an API, a web app, and a self-hosted pipeline. Models in the filtered section are retained only as comparison references, not as uncensored recommendations.

### Community-reported uncensored variants

These entries are included because users report uncensored or low-filter behavior for a particular model version, provider, or local pipeline. The status is endpoint-specific unless the weights are available for local inference.

| Model / variant | Release / update | Access | Why it belongs here | Status | Official source |
| --- | --- | --- | --- | --- | --- |
| Seedream 2.0 / 3.0 / 4.0 / 4.5 / 5.0 Lite / Pro | 2024-12 onward | Hosted / API | Community-reported uncensored behavior on selected providers; exact endpoint and version matter | Community-reported | [Seed models](https://seed.bytedance.com/en/models) · [3.0 release](https://seed.bytedance.com/en/blog/seedream-3-0-text-to-image-model-technical-report-released) · [4.0 release](https://seed.bytedance.com/en/blog/seedream-4-0-officially-released-beyond-drawing-into-imagination) · [5.0 Lite release](https://seed.bytedance.com/en/blog/deeper-thinking-more-accurate-generation-introducing-seedream-5-0-lite) |
| Qwen Image hosted family: 2.0 / 2.0 Pro / 3.0 / 3.0 Pro / Max / Plus / Edit / Edit Plus / Edit Max and dated snapshots | 2025-12 onward | Hosted / API | Community-reported uncensored behavior for selected Qwen image endpoints and snapshots | Community-reported | [QwenCloud image models](https://docs.qwencloud.com/developer-guides/getting-started/image-models) |
| Wan hosted image family: 2.1 / 2.2 / 2.5 / 2.6 / 2.7 | 2025-2026 | Hosted / API | Community-reported uncensored behavior across selected T2I, I2I, and image-editing endpoints | Community-reported | [QwenCloud image models](https://docs.qwencloud.com/developer-guides/getting-started/image-models) |
| Wan hosted video family: 2.1 / 2.2 / 2.5 / 2.6 / 2.7 | 2025-2026 | Hosted / API / video | Community-reported uncensored behavior for selected T2V, I2V, R2V, animation, and editing endpoints | Community-reported | [QwenCloud video models](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Z-Image / Turbo / Omni-Base / Edit | 2025-11 to 2026-01 | Local weights | Open-weight family with community-reported low-filter local behavior; Omni-Base is intended for customization | Open-weight candidate | [Official repository](https://github.com/Tongyi-MAI/Z-Image) · [Turbo model card](https://huggingface.co/Tongyi-MAI/Z-Image-Turbo) |
| FLUX.1 [schnell] | 2024-08 | Local weights | Apache-2.0 open-weight model that can be run without a hosted provider layer | Open-weight candidate | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-schnell) |
| FLUX.1 [dev] and dev-family variants | 2024-08 onward | Local weights | Open weights for local generation, editing, and control workflows | Open-weight candidate | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-dev) |
| FLUX.2 [klein] 4B / 4B Base | 2026-01-15 | Local weights | Open-weight, fine-tunable, and customizable FLUX models | Open-weight candidate | [Official inference repository](https://github.com/black-forest-labs/flux2) |
| FLUX.2 [klein] 9B / 9B Base / 9B KV | 2026-01-15 | Local weights | Open-weight FLUX variants with local inference and fine-tuning support | Open-weight candidate | [Official inference repository](https://github.com/black-forest-labs/flux2) |
| FLUX.2 [dev] | 2025-11-25 | Local weights | Open-weight generation and editing model; community deployments may remove or replace optional pipeline controls | Open-weight candidate | [Model card](https://huggingface.co/black-forest-labs/FLUX.2-dev) |

### Recent local candidates — uncensored status still requires testing

| Model | Release / update | Access | Why it belongs here | Status | Official source |
| --- | --- | --- | --- | --- | --- |
| HiDream-O1-Image / Dev-2604 | 2026-05 | Local weights | Text-to-image, editing, personalization, and long text layout | To verify per checkpoint and pipeline | [Model card](https://huggingface.co/HiDream-ai/HiDream-O1-Image) |
| HunyuanImage-3.0-Instruct / Distil | 2026-01-26 | Local weights | Prompt reasoning, image-to-image editing, and efficient inference | To verify per checkpoint and pipeline | [Official project](https://github.com/Tencent-Hunyuan/HunyuanImage-3.0) |

### Recent local candidates — 2025 updates

| Model | Release / update | Access | Why it belongs here | Status | Official source |
| --- | --- | --- | --- | --- | --- |
| Qwen Image local family: Qwen-Image / 2512 / Edit-2509 / Edit-2511 / Layered | 2025-07 onward | Local weights | Community-reported low-filter behavior across the downloadable Qwen image checkpoints | Open-weight candidate | [Official project](https://github.com/QwenLM/Qwen-Image) · [model collection](https://huggingface.co/collections/Qwen/qwen-image) |

## Filtered reference models

These models are recent and useful for image-model comparisons, but their provider controls or upstream safety mitigations make them poor fits for an uncensored list. They remain here so the repository does not confuse frontier quality with low filtering.

| Model | Release / update | Access | Why excluded from the uncensored list | Official source |
| --- | --- | --- | --- | --- |
| GPT Image 2 / ChatGPT Images 2.0 | 2026-04-21 | Hosted / API | Provider safety policy and moderation systems | [API model](https://developers.openai.com/api/docs/models/gpt-image-2) · [announcement](https://openai.com/index/introducing-chatgpt-images-2-0/) |
| Gemini 3.1 Flash Image (Nano Banana 2) | 2026 | Hosted / API | Google policy controls and provenance/watermark systems | [Gemini image guide](https://ai.google.dev/gemini-api/docs/image-generation) |
| Gemini 3 Pro Image (Nano Banana Pro) | 2026 | Hosted / API | Google policy controls and hosted-only access | [Gemini image guide](https://ai.google.dev/gemini-api/docs/image-generation) |
| Recraft V4.1 family | 2026-05-30 | Hosted / API | Provider policy; no local model access | [Release](https://www.recraft.ai/press-releases/recraft-v4-1-utility-pro-becomes-the-highest-ranked-text-to-image-model-outside-google-and-openai) |
| Ideogram 4.0 | 2026-06-03 | Open weights / API | The upstream reference pipeline includes safety mitigations; custom local deployments need separate testing | [Release](https://ideogram.ai/news/ideogram-4.0/) · [technical details](https://ideogram.ai/blog/ideogram-4.0/) |
| GPT Image 1.5 | 2025-12-16 | Hosted / API | Provider policy and safety systems | [Announcement](https://openai.com/index/new-chatgpt-images-is-here/) |
| FLUX.2 [pro] / [flex] / [max] | 2025-11-25 onward | Hosted / API | Provider policy and API terms apply | [Release notes](https://docs.bfl.ai/release-notes) |
| Adobe Firefly Image Model 5 | 2025-10-28 | Hosted | Adobe's commercially safe model and provider controls | [Adobe announcement](https://news.adobe.com/news/2025/10/adobe-max-2025-firefly) |
| Nano Banana (Gemini 2.5 Flash Image) | 2025 | Hosted / API | Google policy controls and SynthID watermarking | [Model page](https://ai.google.dev/gemini-api/docs/models/gemini-2.5-flash-image) |
| Imagen 4 | 2025-05-20 | Hosted / API | Google policy controls; hosted lifecycle applies | [Google DeepMind](https://deepmind.google/models/imagen/) |
| Midjourney V7 | 2025-04-30 update | Hosted | Hosted moderation and platform policy | [Official update](https://updates.midjourney.com/v7-update-editor-and-exp/) |
| Ideogram 3.0 | 2025-03-26 | Hosted / API | Hosted moderation and platform policy | [Official release](https://about.ideogram.ai/3.0) |

## Community-reported uncensored variants

Recent model cards and community checkpoints use “uncensored” in several different ways: a modified text encoder, an adult-content fine-tune, removal of an optional safety component, or simply a repository name. The [dedicated uncensored-variants catalog](UNCENSORED-MODELS.md) records the evidence, base model, access requirements, and licensing caveats for each entry.

The strongest recent examples found during the 2026-08-06 review include the Seedream, Qwen Image, and Wan variant families; the open-weight Z-Image and FLUX families; FLUX.2 Klein uncensored text-encoder variants; a Qwen-Image NSFW LoRA; and FLUX.1/SDXL community checkpoints. The [full variant matrix](UNCENSORED-MODELS.md) records the individual versions and endpoint types. These are community or endpoint claims unless the entry is explicitly marked otherwise; local execution does not remove legal or license restrictions.

## Established local baselines

These are established local models that remain useful reference points. Their presence here is not a claim that they are uncensored; verify the exact version, license, and inference pipeline before using or classifying them.

### General-purpose and research models

| Model | Access | Family | Filtering status | Source |
| --- | --- | --- | --- | --- |
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
- **Community-reported endpoint** — users report uncensored behavior for a specific hosted provider, model snapshot, region, or UI; do not generalize it to every deployment of the model family.
- **Open-weight candidate** — the weights can be run or customized locally, but “open-weight” alone is not proof that the model is uncensored.
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
