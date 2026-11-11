# Pair Programming with AI: What Actually Works

**Event:** Nimbus AI Summit 2026 — developer-tools track
**Speaker:** Sara Okafor, Developer Experience
**Session ID:** talk-105
**Recorded:** 2026-10-15

## Transcript

[00:00] I am going to start with a confession: our first internal AI pair-programming rollout was a failure. Adoption peaked at eleven percent and then went down. This talk is about what changed.

[04:30] The failure mode was trust. Developers did not want a tool that edited files behind their back. They wanted a tool that proposed a diff, explained the blast radius and let them reject the change with one keystroke.

[10:15] The second change was repo hygiene. AI assistants get dramatically better when the repository has a test command that runs in under a minute, a clear contributing guide and consistent formatting. We spent a quarter on those and it counted for more than the model upgrade.

[15:45] The third change was measurement. We stopped tracking 'lines accepted' and started tracking 'review cycles saved'. That number survived the finance review, which is the only review that really matters.

[20:20] The open-source tool that shaped our internal design is github.com/Aider-AI/aider. Its repo-map approach and the explicit git-diff workflow were the two ideas our developers kept asking for, and the project's maintainers were unusually responsive to our bug reports.

[27:30] If your AI coding rollout is stuck, it is probably a trust problem, not a model problem. Fix the diff review experience and the adoption curve will follow.
