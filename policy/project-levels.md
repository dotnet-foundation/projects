# Project Levels (Draft)

**Status:** Draft for committee discussion. Not adopted. Everything below is a proposal, open to change.
**Author:** Irina Scurtu
**Date:** 2026-09-10
**See also:** [Evaluation criteria](evaluation-criteria.md) - how a project's level would be decided.

This draft suggests what level a project could enter at and what could happen after. It comes from a gap: the committee records outcomes ("Accept", "Defer", "Decline") without a written rule for what separates them, and "Deferred to Seed" has been used without a definition of what Seed grants or when the project gets looked at again.

---

## Overview

| Level | In short | On the Foundation site | Review |
| --- | --- | --- | --- |
| **Pre-Seed** | Not a Foundation project yet. Closed with written feedback and a reapplication date. | Not listed | None. The applicant reapplies. |
| **Seed** | Admitted at a limited level. The project is in, the expensive services are not. | Listed, labelled `Seed` (open question 1) | At 6 months |
| **Member** | Full project membership. All Foundation services available. | Listed | Health check at 12 months |
| **Declined** | The applicant will not or cannot resolve a [blocking condition](evaluation-criteria.md#blocking-conditions). | Not listed | A cooling-off period before reapplication, suggested at 12 months |

Two project statuses would sit alongside the levels:

| Status | In short |
| --- | --- |
| **Blocked** | Evaluation paused on a fixable [blocking condition](evaluation-criteria.md#blocking-conditions). No level is assigned until it clears. |
| **Conditional** | Member membership held open while the applicant closes a short list of named conditions (see [Member](#member)). |

### What each level could include

| | Pre-Seed | Seed | Member |
| --- | --- | --- | --- |
| Listing on dotnetfoundation.org | - | Labelled `Seed`, if listed at all | Yes |
| A named committee mentor | - | Yes | - |
| CLA infrastructure and governance templates | - | Yes | Yes |
| Community promotion (newsletter, social, standups) | - | Yes | Yes |
| Code signing certificates | - | - | Yes |
| Trademark and IP handling | - | - | Yes |
| Funds, grants, infrastructure credits | - | - | Yes |
| Foundation logo as a project badge | - | `Seed` wording only | Yes |

---

## Pre-Seed

**Overview:** a rejection with a door left open. The applicant gets written feedback and a date to reapply. The committee schedules nothing.

Saying so plainly helps avoid an applicant believing they are "in the Foundation at Seed" when nothing was granted.

The applicant would get:

- A written outcome naming the specific gap, with the metric that produced it.
- A numbered list of conditions for reconsideration, concrete and checkable.
- A reapplication date, not a review date. A possible default is 6 months from the application date, or 9 to 12 months where the gap is track record, since 6 months will not fix a 5-week-old repository.

The applicant would not get: a site listing, use of the Foundation name or logo, CLA infrastructure, code signing, mentorship allocation, or a place on the meeting agenda.

The burden sits with the applicant. That answers the "is it reviewed in 6 months" question for this level with a no. The issue would be closed.

Possible reapplication rules:

- A reapplication filed before the date is closed without evaluation, with a pointer to the date.
- A reapplication states, per condition, what changed and links the evidence. One that repeats the original application is closed without evaluation.
- Two Pre-Seed outcomes on the same project trigger a cooling-off period before a third application, suggested at 12 months.

---

## Seed

**Overview:** membership with the expensive and irreversible services withheld until the project has a track record inside the Foundation. A committee mentor is assigned and the committee reviews the project at 6 months.

A Seed project could get:

- A listing on dotnetfoundation.org, labelled `Seed` (if Seed is listed at all, open question 1).
- CLA infrastructure and governance templates.
- A committee mentor: one named member, recorded in the meeting notes.
- Community promotion (newsletter, social, community standup slots).
- The right to say it is a .NET Foundation Seed project.

A Seed project would not get:

- Code signing certificates.
- Trademark or IP assignment to the Foundation.
- Funds, grants, or infrastructure credits.
- Use of the .NET Foundation logo as a project badge, beyond the `Seed` wording.

The 6-month review would be the committee's job, not the applicant's. For this level the answer to "is it reviewed in 6 months" would be yes.

Possible mechanics:

- The review date is set at admission and recorded in the meeting notes and on the project issue.
- The mentor prepares a delta snapshot: the metric block captured at admission, re-measured, with the difference. Commits, contributors, releases, downloads, open condition items.
- The review has three possible outcomes. Promote to Member, when the capping dimension has moved and the load-bearing criteria are closed. Renew for one further 6-month term, when there is movement in the right direction but not enough of it. Exit, when there is no movement or the maintainer has become unreachable, which would remove the listing and return the project to Pre-Seed with a reapplication date.
- A limit of two terms, so a project would not sit at Seed beyond 12 months (open question 2).
- A long silence from the maintainer, suggested at 60 days, could exit the project.
- If the committee misses the review date, the project stays at Seed and the term pauses. A missed review would not promote or exit a project by default. It moves to the next meeting.

---

## Member

**Overview:** full membership. Everything at Seed, plus code signing, the full logo, IP and trademark handling, and standing in Foundation programmes. A light health check every 12 months.

### Conditional Acceptance

Member status granted with named conditions, all of them from the onboarding group in [Operational hygiene](evaluation-criteria.md#operational-hygiene). Suggested rules:

- Conditions are numbered, checkable, and each one names its evidence link.
- The applicant has a window to close them, suggested at 90 days from the board approval date.
- If they are not closed in that window and the maintainer has not responded, the project could drop to Seed and pick up a 6-month review.
- If they are not closed but the maintainer has engaged and has a plan, one extension could be granted.
- Code signing would wait until every load-bearing criterion is closed.

### Health check

The 12-month health check would be a light pass, not a re-evaluation. The mentor or a rotating reviewer would confirm the project is still active, still licensed as declared, still has a reachable maintainer, and still meets the load-bearing criteria. A failed health check could move the project to a remediation window, then to dormant status if unresolved. The intent is that no Member project is removed without a written warning and that window.

---

## Declined

**Overview:** kept for blocking conditions that can't be solved. Reapplication waits for a cooling-off period, suggested at 12 months.

A project would be Declined only when the applicant will not resolve the condition, provenance cannot be established at all, or the same blocking condition returns on a third application. Everything fixable is handled as Blocked instead. See [Blocking conditions](evaluation-criteria.md#blocking-conditions).

---

## Open questions for the committee

1. Should Seed appear on the site at all? Listing a Seed project lends it the Foundation's credibility before we have any track record with it. A private level with no public listing weakens the incentive to accept Seed instead of arguing for Member.
2. Is 12 months the right cap for Seed, or too short for a volunteer project that is moving slowly but genuinely?
3. Roughly nine projects were "deferred to Seed" with no review ever recorded. Do we run this policy over them, or start clean from the adoption date?
4. Are the suggested time windows (60 days silence at Seed, 90 days for conditions, 12-month cooling-off) the right ones?
