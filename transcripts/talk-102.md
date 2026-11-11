# Running Frontier Models on a Laptop

**Event:** Nimbus AI Summit 2026 — inference track
**Speaker:** Tomás Ferreira, Local Inference Lab
**Session ID:** talk-102
**Recorded:** 2026-10-14

## Transcript

[00:00] Hello everyone. This session is about the unglamorous side of local inference: downloading a model, loading it without swapping, and keeping the fan noise below the noise of the air conditioning.

[05:20] Quantisation is not a single dial. The right recipe depends on whether you are memory bandwidth bound or compute bound, and most laptops are memory bandwidth bound. That means aggressive quantisation often buys more throughput than a smaller context window.

[11:45] The second lesson is packaging. If a user needs a compiler, a CUDA toolkit and a specific Python version to try your model, you have already lost the hobbyist audience. The installation experience is part of the product.

[16:30] We benchmark on the same three laptops every quarter. It is not scientific, but it keeps us honest about regressions that only show up on integrated GPUs.

[21:10] The runtime we use for these experiments is the one at github.com/ollama/ollama. The single binary install is the reason our test matrix stayed reproducible across machines, and the model registry makes swapping quantisation variants trivial.

[27:30] If you take one thing from this talk, make it this: ship the install command before you ship the benchmark chart. Everything else is a rounding error.
