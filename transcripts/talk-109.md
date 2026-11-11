# Lessons from the Transformer Wars

**Event:** Nimbus AI Summit 2026 — research track
**Speaker:** Prof. Amelia Grant, Applied Research
**Session ID:** talk-109
**Recorded:** 2026-10-17

## Transcript

[00:00] This is a retrospective session. I have spent a decade watching research code become production infrastructure, and I want to talk about what gets lost in that translation.

[05:35] The first lesson is that reference code ages badly. A repository written for one benchmark becomes a compatibility trap for every team that builds on it, because nobody wants to break the community's test scripts.

[11:15] The second lesson is that research artefacts need explicit ownership. When a lab moves on to the next project, the old repository keeps collecting issues and stale pull requests until it is archived. Archival is a kindness, not a failure.

[16:40] The third lesson is evaluation hygiene. We spent years comparing numbers produced by different harnesses, and half the 'improvements' in the literature were artefacts of the harness itself.

[21:20] The research monorepo at github.com/tensorflow/models is the canonical example of scale without a single clear licence: it is enormously influential, but the licensing story across subdirectories is exactly why our legal team refuses a blanket approval.

[24:10] The benchmark API that defined an era was github.com/openai/gym. It is archived now, which is a useful reminder that the interface outlives the codebase and that archiving is how mature projects admit they are done.

[26:45] As a contrast, look at github.com/microsoft/vscode: an enormous consumer-facing repository that still runs a public contribution process. The difference is ownership and process, not age.

[27:30] Research code is a gift, but a gift without a licence and an owner is a future incident. Thank you to everyone who archived their work responsibly.
