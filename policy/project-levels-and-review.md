# Project Levels and Review Policy (Internal Draft)

**Status:** Draft for committee discussion. Not adopted. Everything below is a proposal, open to change.
**Author:** Irina Scurtu
**Date:** 2026-09-10

This draft suggests what level a project could enter at, who might decide, and what could happen after. It comes from a gap: the committee records outcomes ("Accept", "Defer", "Decline") without a written rule for what separates them, and "Deferred to Seed" has been used without a definition of what Seed grants or when the project gets looked at again.

---

## 1. The four levels (proposed)

| Level | What it could mean | On the Foundation site | Review |
| --- | --- | --- | --- |
| **Pre-Seed** | Not a Foundation project. The application would be closed with written feedback and a reapplication date. | Not listed | None. The applicant reapplies. |
| **Seed** | Admitted at a limited level. The project is in, the services are not. | Listed, labelled `Seed` (open question, §9) | At 6 months |
| **Member** | Full project membership. All Foundation services available. | Listed | Health check at 12 months |
| **Declined** | For an applicant who will not or cannot resolve a blocking condition (§2). | Not listed | A cooling-off period before reapplication, suggested at 12 months |

Two project statuses would sit alongside the levels:

| Status | What it could mean |
| --- | --- |
| **Blocked** | Evaluation paused on a fixable blocking condition (§2). No level is assigned until it clears. |
| **Conditional** | Member membership held open while the applicant closes a short list of named conditions (§6). |

---

## 2. Blocking conditions

The suggestion is that any one of these pauses the application where it is. None of them would be a verdict on the project, and every one is fixable by the applicant. The application is parked, not rejected.

| # | Condition | What could resolve it |
| --- | --- | --- |
| 1 | License is not OSI-approved, or is a custom/copyleft license the Foundation cannot accept | Relicense, with sign-off from every copyright holder. Days for a solo project, months where there are many contributors. |
| 2 | Trademark or naming conflict, including org or package names implying Microsoft or Foundation endorsement | Rename the package or org, or produce written permission |
| 3 | Repository is archived, or described by its own author as a showcase, reference, or experiment | Un-archive and state maintenance intent in writing, or withdraw the application |
| 4 | Copyright ownership not affirmed, or provenance of a fork or generated/translated code not established | Affirm in writing; for derived code, document the origin and its license |
| 5 | No commits in the 6 months before evaluation, with no maintainer response | Maintainer responds, states intent, and resumes work |
| 6 | Repository is not public, or no commitment to 2FA on the org | Make it public, enable 2FA |

How it might be handled:

- The evaluator names the condition and its fix in the issue, then marks the application Blocked. It would not be evaluated further, and it would not use up a Pre-Seed cycle (§4).
- The applicant reopens it by showing evidence. Evaluation would then restart at §3 against current metrics. Clearing a blocker would not grant a level. It only makes the level question askable.
- A period of maintainer silence, suggested at 90 days, could close the issue as inactive. Reapplication would stay open at any time, with no cooling-off.

Decline (§1), with its cooling-off, would be kept for cases that can't be solved: the applicant will not resolve the condition, provenance cannot be established at all, or the same blocking condition returns on a third application.

Once §2 is clear, the rest becomes a level question rather than a rejection question.

---

## 3. Entry gates

The idea is to read the level off the application form. Each dimension below maps to fields the applicant fills in, assuming these fields are added to the application template. The evaluator would verify what was declared instead of researching the project from scratch, and the form summary would point strongly toward a level.

| Form field | Feeds |
| --- | --- |
| `license`, `projectStatus`, copyright and 2FA criteria | Blocking conditions (§2) |
| `firstReleaseDate`, `totalCommits` | Track record (§3.1) |
| `maintainerContinuity`, `committers`, `projectLeadPublicProfile` | Continuity (§3.2) |
| `githubStars`, `contributorCount`, `nugetPackages` | Adoption (§3.3) |
| `eligibilityCriteria` and the four evidence URLs, `cla`, `governanceModel` | Hygiene (§3.4) |

A form with blank or contradicted fields could go back to the applicant rather than the evaluator filling the gaps. A field the repository contradicts would be treated as the applicant's answer being wrong, not as new information.

Four dimensions would decide the level, with the lowest one capping it. Under this approach, a project with excellent adoption and a 5-week history would still be Pre-Seed.

### 3.1 Track record

Suggested thresholds:

| Age since first public commit | Ceiling |
| --- | --- |
| Under 6 months | Pre-Seed |
| 6-18 months | Seed |
| Over 18 months | Member |

Age would run from first public commit, not repository creation, and it would be the one date the evaluator confirms against the repository rather than taking `firstReleaseDate` at face value. An application filed within 30 days of the repository going public could be treated as Pre-Seed by default.

### 3.2 Continuity (bus factor)

| Maintainer situation | Ceiling |
| --- | --- |
| Sole maintainer, no succession plan | Seed |
| Sole maintainer with a named successor or an active org | Member, flagged |
| Two or more maintainers with merge rights in the last 6 months | Member |

A single maintainer need not be a reason to decline. What matters is whether anything happens to the project if that person stops. Seed may be a better fit for a project that would stall.

### 3.3 Adoption

| Signal | Ceiling |
| --- | --- |
| No tagged release, or no package published | Pre-Seed |
| Released, but usage is not distinguishable from the maintainer's own CI | Seed |
| Sustained external usage over at least two release cycles | Member |

This deliberately avoids a download number. A niche library at 8,000 downloads can be more adopted than a template at 60,000. The evaluator would write one sentence on whether the usage is real and name the evidence: download curve shape, external issues and PRs, downstream dependents, third-party writeups or conference mentions. Whether to have a floor anyway is an open question (§9).

### 3.4 Operational hygiene

One option is to split the 17 eligibility criteria into two groups.

Load-bearing criteria, expected at Member level and allowed to stay open at Seed: a CLA mechanism, SECURITY.md, an issue tracker with maintainer responses, a public communication channel, documentation sufficient to use the project, dependency licenses cleared.

Onboarding items, allowed to stay open at either level and tracked as conditions: code signing, Source Link, reproducible build, discoverability metadata, home page.

A project failing load-bearing criteria could be capped at Seed until it fixes them. A project failing only onboarding items could be a Member under Conditional Acceptance.

Self-attestation probably shouldn't count on its own. Each eligibility checkbox on the form would need an evidence URL next to it.

---

## 4. Pre-Seed: what could happen

Pre-Seed would be a rejection with a door left open. Saying so plainly helps avoid an applicant believing they are "in the Foundation at Seed" when nothing was granted.

The applicant would get:

- A written outcome naming the specific gap, with the metric that produced it.
- A numbered list of conditions for reconsideration, concrete and checkable.
- A reapplication date, not a review date. A possible default is 6 months from the application date, or 9 to 12 months where the gap is track record, since 6 months will not fix a 5-week-old repository.

The applicant would not get: a site listing, use of the Foundation name or logo, CLA infrastructure, code signing, mentorship allocation, or a place on the meeting agenda.

Under this proposal the committee schedules nothing and the burden sits with the applicant. That answers the "is it reviewed in 6 months" question for this level with a no. The issue would be closed.

Possible reapplication rules:

- A reapplication filed before the date is closed without evaluation, with a pointer to the date.
- A reapplication states, per condition, what changed and links the evidence. One that repeats the original application is closed without evaluation.
- Two Pre-Seed outcomes on the same project trigger a cooling-off period before a third application, suggested at 12 months.

---

## 5. Seed: what could happen

Seed would be membership with the expensive and irreversible services withheld until the project has a track record inside the Foundation.

A Seed project could get:

- A listing on dotnetfoundation.org, labelled `Seed` (if Seed is listed at all, §9).
- CLA infrastructure and governance templates.
- A committee mentor: one named member, recorded in the meeting notes.
- Community promotion (newsletter, social, community standup slots).
- The right to say it is a .NET Foundation Seed project.

A Seed project would not get:

- Code signing certificates.
- Trademark or IP assignment to the Foundation.
- Funds, grants, or infrastructure credits.
- Use of the .NET Foundation logo as a project badge, beyond the `Seed` wording.

The proposal is that the 6-month review is the committee's job, not the applicant's. For this level the answer to "is it reviewed in 6 months" would be yes.

Possible mechanics:

- The review date is set at admission and recorded in the meeting notes and on the project issue.
- The mentor prepares a delta snapshot: the metric block captured at admission, re-measured, with the difference. Commits, contributors, releases, downloads, open condition items.
- The review has three possible outcomes. Promote to Member, when the capping dimension has moved and the load-bearing criteria are closed. Renew for one further 6-month term, when there is movement in the right direction but not enough of it. Exit, when there is no movement or the maintainer has become unreachable, which would remove the listing and return the project to Pre-Seed with a reapplication date.
- A limit of two terms, so a project would not sit at Seed beyond 12 months (open question, §9).
- A long silence from the maintainer, suggested at 60 days, could exit the project.
- If the committee misses the review date, the project stays at Seed and the term pauses. A missed review would not promote or exit a project by default. It moves to the next meeting.

---

## 6. Member and Conditional Acceptance

Member would be full membership: everything at Seed, plus code signing, the full logo, IP and trademark handling, and standing in Foundation programmes.

Conditional Acceptance would be Member status granted with named conditions, all of them from the onboarding group in §3.4. Suggested rules:

- Conditions are numbered, checkable, and each one names its evidence link.
- The applicant has a window to close them, suggested at 90 days from the board approval date.
- If they are not closed in that window and the maintainer has not responded, the project could drop to Seed and pick up a 6-month review under §5.
- If they are not closed but the maintainer has engaged and has a plan, one extension could be granted.
- Code signing would wait until every load-bearing criterion is closed.

The Member health check at 12 months would be a light pass, not a re-evaluation. The mentor or a rotating reviewer would confirm the project is still active, still licensed as declared, still has a reachable maintainer, and still meets the load-bearing criteria. A failed health check could move the project to a remediation window, then to dormant status if unresolved. The intent is that no Member project is removed without a written warning and that window.

---

## 7. Who could decide what

| Decision | Suggested owner |
| --- | --- |
| Blocking condition (§2) | Evaluator, confirmed by one other member, recorded in the notes |
| Decline after an unresolved blocking condition | Committee vote |
| Level assignment | Committee vote at the monthly meeting |
| Conditional Acceptance conditions | Evaluator drafts, committee approves |
| Seed 6-month review outcome | Committee vote, on the mentor's delta snapshot |
| Member health check | Reviewer, escalated to the committee only if it fails |
| Cooling-off waiver | Committee, with a stated reason in the notes |

Quorum has never been defined in the meeting notes. If level assignment becomes a vote, it would need defining (§9).

---

## 8. Recording it

A possible extension of the current meeting note format:

```markdown
### [Project Name](#issue-link)
**Metrics:** N stars · N commits · N contributors · first release YYYY-MM · N downloads
**Capping dimension:** track record / continuity / adoption / hygiene
**Level:** Pre-Seed / Seed / Member / Declined
**Status:** Blocked / Conditional (if any)
**Reason:** one sentence
**Next date:** blocked, awaiting applicant | reapplication YYYY-MM-DD (Pre-Seed) | review YYYY-MM-DD (Seed) | conditions due YYYY-MM-DD
**Mentor:** @handle (Seed only)
```

Naming the capping dimension seems the most useful part. It would make the decision auditable and tell the applicant which of the four things to work on.

---

## 9. Open questions for the committee

1. §3.3 deliberately avoids a number. Do we want a stated adoption floor (total downloads, external contributors, dependents) so borderline calls stay consistent between evaluators, accepting that any number will be wrong for some category of project?
2. Should Seed appear on the site at all? Listing a Seed project lends it the Foundation's credibility before we have any track record with it. A private level with no public listing weakens the incentive to accept Seed instead of arguing for Member.
3. What is quorum for a level vote, and can an evaluator vote on their own evaluation?
4. Roughly nine projects were "deferred to Seed" with no review ever recorded. Do we run this policy over them, or start clean from the adoption date?
5. Transfers and sunsets. A Microsoft handover arrives with maturity but often without a maintainer. Does it enter at Member on its metrics, or at Seed until continuity is proven under new ownership? One reading is Seed, since §3.2 is the failing dimension and the one that decides whether the project survives.
6. Is 12 months the right cap for Seed, or too short for a volunteer project that is moving slowly but genuinely?
7. Are the suggested time windows (90 days blocked, 60 days silence, 90 days for conditions, 12-month cooling-off) the right ones?
