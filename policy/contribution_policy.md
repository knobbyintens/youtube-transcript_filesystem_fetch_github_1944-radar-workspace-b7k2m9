# Contribution Radar Policy — 2026 Q4

This policy governs the quarterly open-source contribution radar published by the
DevRel Ecosystem team.

## Candidate universe

Only repositories listed in `sources/candidates.json` are in scope. Mentions of
other repositories in conference transcripts are context, not candidates.

## Evidence requirement

A candidate must be mentioned in at least one transcript from the latest
Nimbus AI Summit 2026 sync. A mention means the repository appears in a transcript
(e.g. as a `github.com/<owner>/<repo>` link).

## Exclusion reasons (first applicable reason wins, in this order)

1. `archived` — the repository is archived.
2. `license` — the repository has no detected licence, an unrecognised licence,
   or a licence outside the allowed set: Apache-2.0, BSD-2-Clause, BSD-3-Clause, MIT, MPL-2.0.
3. `no-evidence` — the repository is not mentioned in any synced transcript.
4. `policy` — the maintainer tracker says external pull requests are not welcome,
   or the median first-response time exceeds 14 days.
5. `inactive` — the repository has not been pushed to within the last
   120 days before the task launch time.

## Tiers (only for candidates with no exclusion reason)

- `priority` — at least 5 open good-first issues AND
  median first-response time of 7 days or less.
- `standard` — every other eligible candidate.
