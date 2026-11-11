# Coding Agents in the Enterprise

**Event:** Nimbus AI Summit 2026 — developer-tools track
**Speaker:** Kenji Watanabe, Security Engineering
**Session ID:** talk-108
**Recorded:** 2026-10-16

## Transcript

[00:00] My job is to say no to things, so this talk is about how a coding agent earned a conditional yes from a security team that had every reason to be sceptical.

[04:50] The first requirement was a complete local audit trail. Every command, every file write and every network call has to be attributable to a session and a human approver. Without that, procurement will not even open the review.

[10:40] The second requirement was a secrets story. An agent that can read a developer's shell history is an agent that can exfiltrate a cloud key in a tool call. Short-lived credentials and an explicit deny list are not optional.

[16:20] The third requirement was revocation. We needed a single switch that stops all agent sessions in a business unit within seconds, and we needed to test that switch every quarter.

[21:05] The tool our pilot teams used is github.com/anthropics/claude-code. It gave us a familiar terminal workflow, but we had to wrap it in our own policy layer to satisfy the audit requirements above. Note that the repository does not publish an explicit source-license file, which matters for our legal review.

[27:30] Security never gets to be an afterthought in an agent platform. If you build the audit trail first, the rest of the review becomes a checklist instead of a negotiation.
