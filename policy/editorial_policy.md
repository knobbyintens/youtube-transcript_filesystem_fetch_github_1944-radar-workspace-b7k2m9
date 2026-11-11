# Editorial Curation Policy v2

This policy governs how candidate videos from the partner network are evaluated for the learning
library. Apply the rules in the order listed below. The first rule that matches determines the
final outcome; never continue evaluating a candidate once it has been rejected.

## Rule 1 - Category scope

Only the following YouTube category IDs are in scope:

- `27` - Education
- `28` - Science & Technology

Any other category is rejected with reason `category_out_of_scope`.

## Rule 2 - Live programming

Videos whose live broadcast state is `live` or `upcoming` are rejected with reason
`live_or_upcoming`. Only regular, released videos are eligible.

## Rule 3 - Blocked title keywords

The following keywords must not appear anywhere in the video title (case-insensitive):

- `illegal`
- `leak`
- `spoiler`
- `nsfw`

A matching title is rejected with reason `blocked_keyword`.

## Rule 4 - Minimum duration

Videos shorter than 120 seconds are rejected with reason `too_short`.

## Rule 5 - Format slot

Eligible videos are assigned a format slot based on duration:

- 120 to 300 seconds inclusive: `quick_tip`
- 301 to 1200 seconds inclusive: `standard`
- longer than 1200 seconds: `deep_dive`

## Rule 6 - Review for long form from unverified channels

A `deep_dive` video whose channel is not on the preferred channel list must be sent to editorial
review: status `needs_review`, reason `long_form_unverified_channel`. Do not approve it directly.

## Rule 7 - Approval and priority

All remaining eligible videos are approved with reason `ok`. Approved videos from a preferred
channel get priority `high`; approved videos from any other channel get priority `normal`.

## Preferred channels

- `UCWv7vMbMWH4-V0ZXdmDpPBA` (Programming with Mosh)
- `UCsBjURrPoezykLs9EqgamOA` (Fireship)
- `UCKWaEZ-_VweaEx1j62do_vQ` (IBM Technology)

## Output rules

- Every candidate receives exactly one final status: `approved`, `needs_review` or `rejected`.
- Rejected candidates have no format slot and priority `none`.
- Candidates that need review have priority `none`.
- Approved candidates use reason `ok` and a priority of `high` or `normal`.

## Repository output conventions

- `pipeline/queue_status.json` must be a JSON array of objects with `video_id` and `status`.
- `reports/curation_report.json` must be a JSON array using the same field set as the decision
  report: `video_id`, `title`, `channel_id`, `category_id`, `duration_seconds`, `format`,
  `status`, `priority`, `reason`.
- `pipeline/rejected.json` must be a JSON array of objects with `video_id` and `reason`, listing
  only rejected candidates.
- Every candidate that lands in `needs_review` must get a repository work item titled
  `[Editorial Review] <video_id>` with the label `editorial-review`. The work item body must
  contain the video ID, the title, the duration in seconds and the reason code.
