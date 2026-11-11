# Model Hub Operations at Scale

**Event:** Nimbus AI Summit 2026 — ml-infra track
**Speaker:** Ivan Petrov, ML Infrastructure
**Session ID:** talk-106
**Recorded:** 2026-10-16

## Transcript

[00:00] Hello. My team runs the model registry and the download mirror for a few thousand internal users. This is a talk about supply chain, caching and the one incident that taught us to respect checksums.

[05:10] Model artefacts are big, immutable and frequently re-downloaded. The only sane architecture is content-addressed storage with an aggressive regional cache, because a hot model file can account for more egress than an entire product team's API traffic.

[11:30] The second lesson is provenance. Every artefact needs a signed origin, a license record and a clear owner. When legal asks who approved a model for production, 'it was on the hub' is not an acceptable answer.

[17:05] The third lesson is pinning. Floating refs are convenient until a weekend rollout silently picks up a new tokenizer and the evaluation numbers move. Pin the hash, then promote.

[22:40] The library our serving teams standardise on is github.com/huggingface/transformers. The model definition registry is what lets us keep a single serving contract while the underlying checkpoints evolve, and the maintainers run a serious release process.

[27:30] Treat model files like production dependencies, because they are. Checksums, licenses and owners are not paperwork; they are the difference between a platform and a liability.
