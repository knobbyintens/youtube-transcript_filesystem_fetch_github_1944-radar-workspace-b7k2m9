# Multi-Agent Orchestration: Patterns and Pitfalls

**Event:** Nimbus AI Summit 2026 — agents track
**Speaker:** Dr. Lena Hoffmann, Research Engineering
**Session ID:** talk-107
**Recorded:** 2026-10-16

## Transcript

[00:00] Multi-agent systems are a wonderful demo and a difficult product. Today I want to walk through three patterns that survived contact with real users and two that did not.

[06:20] The pattern that survived is the supervisor with bounded delegation. A supervisor owns the plan, sub-agents own narrow tools, and every message between them is logged. The bound on delegation is what prevents runaway token spend.

[12:10] The pattern that did not survive was the free-for-all debate. It produced beautiful transcripts and terrible latency, and nobody could explain why a conclusion had been reached.

[18:05] The second survivor is deterministic replay. If you cannot replay the exact sequence of agent messages for a failed task, you cannot debug it, and if you cannot debug it you cannot put it in front of a customer.

[23:15] Our reference for the supervisor pattern was github.com/microsoft/autogen. The group-chat abstraction gave us a vocabulary for bounded delegation, even though we ended up reimplementing the scheduler for our own SLA requirements.

[27:30] Start with one agent and a good audit log. Add a second agent only when the first one can articulate exactly what it cannot do. That is the entire lesson.
