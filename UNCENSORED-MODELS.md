# Community-Labeled Uncensored Image Models

> A source-tracked list of local image checkpoints, LoRAs, and text-encoder variants whose creators or repository metadata describe them as uncensored, low-filter, or NSFW-capable.

**Last reviewed:** 2026-08-05

## Read this first

“Uncensored” is a claim about behavior, not a standardized model property. It may mean that a text encoder no longer refuses prompts, that a checkpoint was fine-tuned on adult imagery, or that an optional safety checker is not included. These are different things.

This page records upstream claims and available metadata. It does not independently certify output behavior, provenance, legality, or safety. Do not infer commercial permission from the availability of weights.

## Evidence levels

- **Creator-labeled** — the model card explicitly describes the modification or removal of a safety/refusal mechanism.
- **Community-labeled** — the repository name, tags, or surrounding metadata make the claim, but the card does not provide enough reproducible detail.
- **Adapter** — this is a LoRA or text encoder and must be combined with its stated base model.
- **Needs review** — the source is discoverable but lineage, license, or behavior is not documented well enough for a stronger classification.

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
