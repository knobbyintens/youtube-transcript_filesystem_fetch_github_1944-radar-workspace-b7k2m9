# Composable Agent Stacks in Production

**Event:** Nimbus AI Summit 2026 — agents track
**Speaker:** Priya Raghavan, Applied AI
**Session ID:** talk-103
**Recorded:** 2026-10-15

## Transcript

[00:00] Thanks for being here. I run a team that ships internal agent workflows, and today I want to argue that the framework wars are mostly a distraction. The interesting work is in the seams between orchestration, serving and observability.

[03:15] We structure every workflow as a graph of typed steps. Typed steps are what let us swap an orchestration library without rewriting the business logic, and they make evaluation sets reusable across teams.

[08:40] On the serving side, throughput per dollar is the metric that survives the first budget review. Once you move from a demo to a product, you are in the batching and scheduling business whether you like it or not.

[13:20] The last piece is an explicit escalation policy. An agent that cannot hand a task back to a human with a readable summary is an agent that will eventually page the wrong person at two in the morning.

[17:05] For the orchestration layer we used github.com/crewAIInc/crewAI as a reference for role based collaboration. It gave us a clean vocabulary for hand-offs, and the community brought us several fixes we would not have written ourselves.

[22:25] On the serving tier, our benchmark harness targets github.com/vllm-project/vllm. Continuous batching and the paged attention scheduler are the reason we could cut GPU spend without cutting the quality bar.

[27:30] Composability sounds like an architecture slogan, but in practice it is a procurement strategy: you want to be able to replace any layer without a re-platforming project. Build for the seams.
