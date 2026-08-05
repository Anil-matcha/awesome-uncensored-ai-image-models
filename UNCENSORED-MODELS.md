# Uncensored / Low-Filter Image Models

> A source-tracked list of local checkpoints, open-weight models, LoRAs, text-encoder variants, and community-reported hosted endpoints whose creators or users describe them as uncensored, low-filter, or NSFW-capable.

**Last reviewed:** 2026-08-06

## Read this first

“Uncensored” is a claim about behavior, not a standardized model property. It may mean that a text encoder no longer refuses prompts, that a checkpoint was fine-tuned on adult imagery, or that an optional safety checker is not included. These are different things.

This page records upstream claims and available metadata. It does not independently certify output behavior, provenance, legality, or safety. Do not infer commercial permission from the availability of weights.

Hosted/API entries are intentionally included when users report uncensored behavior for a specific endpoint. The provider, region, model snapshot, UI, and date must be recorded because another endpoint using the same model name may behave differently.

## Evidence levels

- **Creator-labeled** — the model card explicitly describes the modification or removal of a safety/refusal mechanism.
- **Community-labeled** — the repository name, tags, or surrounding metadata make the claim, but the card does not provide enough reproducible detail.
- **Adapter** — this is a LoRA or text encoder and must be combined with its stated base model.
- **Community-reported endpoint** — users report uncensored behavior for a particular hosted provider or API, but the claim has not been independently reproduced by this repository.
- **Needs review** — the source is discoverable but lineage, license, or behavior is not documented well enough for a stronger classification.

## Community-reported hosted/API variants

| Model / variant | Access | Model identity / requirement | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| Seedream 2.0 / 3.0 / 4.0 / 4.5 / 5.0 Lite / Pro | Hosted / API | ByteDance Seedream family | Community-reported endpoint | Included as uncensored endpoint reports; record the exact provider, model version, region, and date. | [Seed models](https://seed.bytedance.com/en/models) · [2.0 report](https://seed.bytedance.com/blog/doubao-text-to-image-technical-report-released-full-disclosure-of-data-processing-pre-training-and-rlhf-workflow) · [3.0 release](https://seed.bytedance.com/en/blog/seedream-3-0-text-to-image-model-technical-report-released) · [4.0 release](https://seed.bytedance.com/en/blog/seedream-4-0-officially-released-beyond-drawing-into-imagination) · [5.0 Lite release](https://seed.bytedance.com/en/blog/deeper-thinking-more-accurate-generation-introducing-seedream-5-0-lite) |
| Qwen Image hosted family | Hosted / API | `qwen-image-3.0`, `qwen-image-3.0-pro`, `qwen-image-2.0`, `qwen-image-2.0-2026-03-03`, `qwen-image-2.0-pro`, `qwen-image-2.0-pro-2026-03-03`, `qwen-image-2.0-pro-2026-04-22`, `qwen-image-2.0-pro-2026-06-22`, `qwen-image-max`, `qwen-image-max-2025-12-30`, `qwen-image-plus`, `qwen-image-plus-2026-01-09`, `qwen-image`, `qwen-image-edit`, `qwen-image-edit-plus`, `qwen-image-edit-plus-2025-10-30`, `qwen-image-edit-plus-2025-12-15`, `qwen-image-edit-max`, and `qwen-image-edit-max-2026-01-16` | Community-reported endpoint | Includes the reported Qwen Image variants; exact endpoint and snapshot are part of the claim. | [QwenCloud image models](https://docs.qwencloud.com/developer-guides/getting-started/image-models) |
| Wan hosted image family | Hosted / API | `wan2.7-image[-pro]`, `wan2.6-image`, `wan2.6-t2i`, `wan2.5-t2i-preview`, `wan2.5-i2i-preview`, `wan2.2-t2i-plus`, `wan2.2-t2i-flash`, `wan2.1-t2i-plus`, and `wan2.1-t2i-turbo` | Community-reported endpoint | Includes text-to-image, image-to-image, and image-editing variants reported as uncensored by users. | [QwenCloud image models](https://docs.qwencloud.com/developer-guides/getting-started/image-models) · [Wan image editing](https://docs.qwencloud.com/developer-guides/image-generation/wan-image-editing) |
| Wan hosted video family | Hosted / API / video | Wan 2.7: `t2v`, `t2v-2026-04-25`, `t2v-2026-06-12`, `i2v`, `i2v-2026-04-25`, `r2v-2026-06-12`, `videoedit`; Wan 2.6: `t2v`, `i2v`, `i2v-flash`, `r2v`, `r2v-flash`; Wan 2.5: `t2v-preview`, `i2v-preview`; Wan 2.2: `t2v-plus`, `i2v-plus`, `i2v-flash`, `kf2v-flash`, `animate-move`, `animate-mix`; Wan 2.1: `t2v-plus`, `t2v-turbo`, `i2v-plus`, `i2v-turbo`, `kf2v-plus`, `vace-plus` | Community-reported endpoint | Included for the image-to-video and video scope; endpoint behavior is provider-specific. | [QwenCloud video models](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Z-Image-Turbo API | Hosted / API | `Tongyi-MAI/Z-Image-Turbo` or provider deployment | Community-reported endpoint | Separate from local Z-Image weights; hosted wrapper controls may differ. | [QwenCloud image models](https://docs.qwencloud.com/developer-guides/getting-started/image-models) · [Model card](https://huggingface.co/Tongyi-MAI/Z-Image-Turbo) |

## Official open-weight families included as uncensored candidates

These are included because they can be downloaded or run locally. “Open-weight” describes access and customization, not a guarantee of unrestricted behavior; community fine-tunes, text encoders, and pipeline choices can change results.

| Model / variant | Type | Base / requirement | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| Qwen-Image / 2512 / Edit-2509 / Edit-2511 / Layered | Open-weight family | Qwen Image pipeline | Community-reported low-filter local behavior | Official repository lists Apache-2.0; check each derivative card separately. | [Official project](https://github.com/QwenLM/Qwen-Image) · [Model collection](https://huggingface.co/collections/Qwen/qwen-image) |
| Z-Image / Z-Image-Turbo / Omni-Base / Edit | Checkpoint family | Tongyi-MAI Z-Image pipeline | Open-weight candidate; Omni-Base is described as a raw community fine-tuning base | Apache-2.0 on the official Turbo model card; verify derivative terms. | [Official repository](https://github.com/Tongyi-MAI/Z-Image) · [Turbo model card](https://huggingface.co/Tongyi-MAI/Z-Image-Turbo) |
| FLUX.1 [schnell] | Checkpoint | FLUX.1 pipeline | Open-weight candidate for local inference | Apache-2.0, with the upstream acceptable-use restrictions. | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-schnell) |
| FLUX.1 [dev] and dev-family variants | Checkpoint family | FLUX.1 pipeline | Open-weight candidate for local generation, editing, and control workflows | FLUX.1 dev non-commercial license; review terms for derivatives such as Kontext, Fill, Depth, Canny, and Redux. | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-dev) |
| FLUX.2 [klein] 4B / 4B Base | Checkpoint family | FLUX.2 pipeline | Open-weight candidate; supports local generation and editing | Apache-2.0 according to the official FLUX.2 repository. | [Official inference repository](https://github.com/black-forest-labs/flux2) |
| FLUX.2 [klein] 9B / 9B Base / 9B KV | Checkpoint family | FLUX.2 pipeline | Open-weight candidate; supports local generation and editing | FLUX non-commercial license; review filtering/manual-review requirements before deployment. | [Official inference repository](https://github.com/black-forest-labs/flux2) |
| FLUX.2 [dev] | Checkpoint | FLUX.2 pipeline | Open-weight candidate; community deployments may alter pipeline controls | FLUX non-commercial license; the upstream card documents safety fine-tuning and inference-filter requirements. | [Model card](https://huggingface.co/black-forest-labs/FLUX.2-dev) |
| Wan2.1 local family | Video / image-to-video checkpoints | T2V-14B, I2V-14B-720P, I2V-14B-480P, T2V-1.3B, FLF2V-14B, VACE-1.3B, VACE-14B | Open-weight candidate | Apache-2.0; included for local video and image-to-video scope. | [Official Wan2.1 repository](https://github.com/Wan-Video/Wan2.1) |
| Wan2.2 local family | Video / image-to-video checkpoints | T2V-A14B, I2V-A14B, TI2V-5B, S2V-14B, Animate-14B | Open-weight candidate | Apache-2.0; included for local video, image-to-video, speech-to-video, and animation scope. | [Official Wan2.2 repository](https://github.com/Wan-Video/Wan2.2) |

## Recent community variants

| Model | Type | Base / requirement | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| FLUX.2 Klein 4B Uncensored Text Encoder | Text-encoder adapter | FLUX.2 Klein 4B | Creator-labeled | The card says it removes refusal behavior from the text encoder; the official FLUX.2 Klein DiT is still required. Check the current FLUX terms before use. | [Model card](https://huggingface.co/ponpoke/flux2-klein-4b-uncensored-text-encoder) |
| FLUX.2 Klein 9B Uncensored Text Encoder | Text-encoder adapter | FLUX.2 Klein 9B | Creator-labeled | Same approach as the 4B variant; the 9B base has FLUX non-commercial terms. | [Model card](https://huggingface.co/ponpoke/flux2-klein-9b-uncensored-text-encoder) |
| FLUX.2 Klein Base 9B Bucket Uncensored | Checkpoint | FLUX.2 Klein 9B Base | Community-labeled | The card identifies a 9B local checkpoint and retains FLUX restrictions, including prohibitions on illegal and non-consensual intimate imagery. Verify lineage and behavior before classification. | [Model card](https://huggingface.co/darknight9121/FLUX.2-klein-base-9B-bucket-uncensored) |
| Qwen-Image-NSFW | LoRA | Qwen/Qwen-Image | Creator-labeled | The card identifies it as a Qwen-Image LoRA and lists Apache-2.0; confirm the base-model and derivative terms before redistribution. | [Model card](https://huggingface.co/starsfriday/Qwen-Image-NSFW) |
| FHDR_Uncensored | Checkpoint | FLUX.1-dev | Creator-labeled | 12B FluxPipeline checkpoint; the Hub shows an `other` license and gated access, so commercial use should be treated as unresolved. | [Model card](https://huggingface.co/kpsss34/FHDR_Uncensored) |
| Flux_Lustly.ai_Uncensored_nsfw_v1 | LoRA | FLUX.1-dev | Creator-labeled | The card provides a local Diffusers LoRA workflow and lists CreativeML OpenRAIL-M. Check both the adapter terms and the FLUX base-model terms. | [Model card](https://huggingface.co/lustlyai/Flux_Lustly.ai_Uncensored_nsfw_v1) |
| Flux-NSFW-uncensored | Checkpoint / adapter | FLUX family; verify exact base | Community-labeled | The Hub marks it sensitive and lists CreativeML OpenRAIL-M, but the visible card is sparse. Verify the exact files and lineage. | [Model card](https://huggingface.co/Heartsync/Flux-NSFW-uncensored) |
| Flux-uncensored | LoRA / adapter | FLUX.1-dev | Community-labeled | The card loads it as a LoRA and lists CreativeML OpenRAIL-M; no independent behavior test is recorded here. | [Model card](https://huggingface.co/kp-forks/Flux-uncensored) |
| Uncensored_Base | LoRA / adapter | FLUX.1-dev | Community-labeled | The Hub identifies it as a FLUX.1-dev adapter under CC BY-NC-ND 4.0. The non-commercial/no-derivatives terms matter. | [Model card](https://huggingface.co/Keltezaa/Uncensored_Base) |
| Illustrious XL Improved Uncensored v3.0 | Checkpoint | Illustrious XL / SDXL | Community-labeled | The card lists Fair AI Public License 1.0-SD but is largely auto-generated; treat the uncensored claim and training lineage as unverified. | [Model card](https://huggingface.co/John6666/illustrious-xl10-improved-uncensored-v30-sdxl) |
| PonyRealism-Uncensored | Checkpoint | SDXL / Pony family; verify | Needs review | The repository is labeled uncensored, but its auto-generated card does not document a clear license, base lineage, or safety evaluation. | [Model card](https://huggingface.co/nesaorg/PonyRealism-Uncensored) |

## What this list does not claim

- A text-encoder modification does not guarantee that the image transformer learned every concept.
- A local checkpoint is not automatically free of UI, pipeline, or optional safety filters.
- “NSFW” or “uncensored” tags do not grant permission to create illegal or non-consensual material.
- A model's license does not automatically transfer to its base model, training data, outputs, or hosted deployment.

## Safety boundary

Use these resources only for lawful, consensual, and ethical work. Do not create sexual content involving minors, non-consensual intimate imagery, targeted harassment, fraud, impersonation, or other abusive or illegal material. Do not submit real-person sexual examples or personal data to this repository.

## How to add a variant

Open an issue using the [model submission template](.github/ISSUE_TEMPLATE/model-submission.md). Include the exact model ID, base model, file/version, evidence for the uncensored claim, license, and a reproducible local setup. Prefer source links over screenshots or search-result snippets.
