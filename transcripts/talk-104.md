# The Efficient Inference Stack

**Event:** Nimbus AI Summit 2026 — inference track
**Speaker:** Jonas Weber, Performance Engineering
**Session ID:** talk-104
**Recorded:** 2026-10-15

## Transcript

[00:00] This is a performance talk, so I will show charts. My promise is that each chart comes with a number that you can reproduce on a single node.

[06:05] The baseline matters more than the optimisation. We spent two weeks building a deterministic load generator, and it paid for itself in the first afternoon because half of our apparent regressions were measurement noise.

[12:50] The second axis is portability. Kernels that only run on one vendor's accelerator are research, not infrastructure. The engineering cost of a second backend is real, but so is the cost of a deployment that cannot move.

[18:15] Finally, treat memory layout as an API. Once you promise a tensor layout to downstream users, changing it becomes a breaking change, even if the numerics are identical.

[23:40] The reference implementation for the CPU and edge path is github.com/ggml-org/llama.cpp. It is a masterclass in keeping a portable kernel library honest, and its quantisation tooling is what let us ship a consistent runtime across AMD, Apple and x86 boxes.

[27:30] Optimisation without a reproducible baseline is just folklore. Build the load generator first, then argue about kernels. Thanks to the maintainers who patiently reviewed our first terrible patch to the project.
