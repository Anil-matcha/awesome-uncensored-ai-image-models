# Awesome Uncensored AI Image Models

> A community-maintained catalog of open and low-filter AI image models, checkpoints, and local inference resources.

"Uncensored" is not a standardized technical term. A model's behavior can change with the checkpoint, prompt wrapper, inference UI, safety checker, and version. This list records those details instead of treating the label as a guarantee.

## Contents

- [Starter catalog](#starter-catalog)
- [How entries are classified](#how-entries-are-classified)
- [What each entry should include](#what-each-entry-should-include)
- [Contributing](#contributing)
- [Responsible use](#responsible-use)

## Starter catalog

These are seed entries for the catalog. Their presence here is not a claim that they are uncensored; verify the exact version, license, and inference pipeline before using or submitting a classification.

### General-purpose and research models

| Model | Family | Filtering status | Source |
| --- | --- | --- | --- |
| FLUX.1 [dev] | FLUX | To verify | [Model card](https://huggingface.co/black-forest-labs/FLUX.1-dev) |
| Stable Diffusion XL Base 1.0 | SDXL | To verify | [Model card](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0) |
| Stable Diffusion v1.5 | Stable Diffusion | To verify | [Model card](https://huggingface.co/runwayml/stable-diffusion-v1-5) |
| PixArt-Σ | PixArt | To verify | [Model card](https://huggingface.co/PixArt-alpha/PixArt-Sigma-XL-2-1024-MS) |
| Playground v2.5 | Playground | To verify | [Model card](https://huggingface.co/playgroundai/playground-v2.5-1024px-aesthetic) |

### Community checkpoints and fine-tunes

| Model | Focus | Filtering status | Source |
| --- | --- | --- | --- |
| DreamShaper XL 1.0 | General / stylized | To verify | [Model card](https://huggingface.co/Lykon/dreamshaper-xl-1-0) |
| Animagine XL 3.1 | Anime / illustration | To verify | [Model card](https://huggingface.co/cagliostrolab/animagine-xl-3.1) |

Want to add a model? Use the [submission template](.github/ISSUE_TEMPLATE/model-submission.md) or open a pull request.

## How entries are classified

- **Verified low-filter** — the exact checkpoint and inference setup are documented, and a maintainer has reproduced the reported behavior.
- **Community-reported** — a contributor has supplied reproducible details, but a maintainer has not independently checked them yet.
- **To verify** — the model is a useful catalog candidate, but its filtering behavior or licensing details still need documentation.
- **Removed** — the source is unavailable, the license is unclear, or the entry repeatedly fails the contribution requirements.

These labels describe observed behavior and documentation quality. They do not grant permission to create, distribute, or use any particular content.

## What each entry should include

Every accepted entry should document:

- exact model and checkpoint version;
- official source and download links;
- base architecture and intended use;
- license, commercial-use terms, and restrictions;
- approximate VRAM or hardware requirements;
- supported inference tools or workflows;
- whether filtering is in the weights, the pipeline, the UI, or an optional safety checker;
- reproducible notes about testing, including date and setup.

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a model. Short version: cite primary sources, preserve license information, avoid vague “uncensored” claims, and keep entries factual and reproducible.

## Responsible use

Use these resources for lawful, consensual, and ethical creative or research work. Do not use them to create sexual content involving minors, non-consensual intimate imagery, targeted harassment, fraud, impersonation, or other abusive or illegal material. Follow the model license and the laws that apply to you.

## License

The original documentation and catalog content in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Individual models remain subject to their own licenses and terms.
