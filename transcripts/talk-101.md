# Agents That Ship: From Terminal to Production

**Event:** Nimbus AI Summit 2026 — agents track
**Speaker:** Dr. Maya Chen, Platform Engineering
**Session ID:** talk-101
**Recorded:** 2026-10-14

## Transcript

[00:00] Okay, we're live. Thanks for coming to the opening agents session. I want to talk about the gap between a demo that impresses and an agent that survives a Monday morning on-call rotation.

[04:10] The first thing we learned is that the terminal is still the best interface for accountability. Every action a coding agent takes should leave a readable trace in a shell session, and every tool call should be reviewable before it touches a shared branch.

[09:30] The second thing is sandboxing. We moved from shared developer laptops to disposable containers because the blast radius of a bad tool call is much larger than people expect. Nine out of ten incidents we saw at the company started with an agent that had write access to everything and no ability to explain what it was doing.

[14:05] Our workflow now is boring on purpose: plan, diff, ask for approval, execute, verify. Boring workflows are how you get adoption from security teams, and adoption from security teams is what makes an agent platform real.

[18:40] The coding agent we standardised on is the open-source project at github.com/openai/codex. We use it in the terminal because it keeps the plan/diff loop visible to reviewers, and it plays nicely with our internal sandbox images.

[23:55] For teams that want a batteries-included CLI, we also evaluated github.com/google-gemini/gemini-cli. It is a solid reference implementation for tool registration and session replay, and the contribution surface is friendly to external maintainers.

[27:30] So the takeaway is not 'pick the best model'. The takeaway is 'pick an agent runtime that makes audit easy'. If the transcript of a session can't be handed to an incident reviewer, the agent is a liability. Thanks, and I'll be at the hallway track after this.
