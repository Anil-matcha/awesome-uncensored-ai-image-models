# Contributing

Thanks for helping keep this list accurate and useful.

## Add a model

Before opening a pull request:

1. Check that the model is publicly available from a reputable source.
2. Link to the official model card or repository whenever possible.
3. Record the exact checkpoint, version, and inference setup you tested.
4. Record the release date or most recent major update.
5. Identify whether access is local, hosted, API-only, or available in multiple forms.
6. Include the license, commercial-use terms, provider terms, and restrictions from the source.
7. Describe filtering precisely. Separate model behavior from UI settings, provider policy, and optional safety checkers.
8. If calling a model “uncensored,” cite the exact upstream evidence and say whether it is a full checkpoint, LoRA, or text-encoder modification.
9. Do not include private datasets, personal information, or explicit examples involving real people.

Use the [model submission issue template](.github/ISSUE_TEMPLATE/model-submission.md) if you are unsure whether an entry is ready.

## Pull request checklist

- [ ] The source link works.
- [ ] The exact version or commit is identified.
- [ ] Release date or latest major update is identified.
- [ ] Access method is identified: local, hosted, API, or mixed.
- [ ] License and provider terms are included.
- [ ] Hardware and inference details are included where known.
- [ ] “Uncensored” claims are supported by reproducible notes.
- [ ] The base model and adapter/checkpoint relationship is clear.
- [ ] The entry does not encourage illegal or abusive use.
- [ ] The README remains alphabetized within its category where practical.

## Corrections and removals

Open an issue when a link, license, or behavior description is outdated. Include the affected version and a source for the correction. We may remove entries with unclear provenance, incompatible licensing, or repeated inaccurate claims.
