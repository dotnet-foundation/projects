# Evaluation Criteria (Draft)

**Status:** Draft for committee discussion. Not adopted. Everything below is a proposal, open to change.
**Author:** Irina Scurtu
**Date:** 2026-09-10
**See also:** [Project levels](project-levels.md) - what each level means and what happens after.

This draft suggests how an application could be evaluated: what stops it, what decides its level, who decides, and how the outcome is recorded.

---

## How an evaluation would run

1. Check the [blocking conditions](#blocking-conditions). If any applies, the application is marked Blocked and goes no further until it is fixed.
2. Score the four [dimensions](#the-four-dimensions) from the application form. The lowest one caps the level.
3. The committee votes on the level at the monthly meeting (see [Who could decide what](#who-could-decide-what)).
4. Record the outcome in the meeting notes (see [Recording it](#recording-it)).

---

## Blocking conditions

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

- The evaluator names the condition and its fix in the issue, then marks the application Blocked. It would not be evaluated further, and it would not use up a Pre-Seed cycle.
- The applicant reopens it by showing evidence. Evaluation would then restart against current metrics. Clearing a blocker would not grant a level. It only makes the level question askable.
- A period of maintainer silence, suggested at 90 days, could close the issue as inactive. Reapplication would stay open at any time, with no cooling-off.

[Declined](project-levels.md#declined), with its cooling-off, would be kept for cases that can't be solved: the applicant will not resolve the condition, provenance cannot be established at all, or the same blocking condition returns on a third application.

Once the blocking conditions are clear, the rest becomes a level question rather than a rejection question.

---

## The four dimensions

The idea is to read the level off the application form. Each dimension below maps to fields the applicant fills in, assuming these fields are added to the application template. The evaluator would verify what was declared instead of researching the project from scratch, and the form summary would point strongly toward a level.

| Form field | Feeds |
| --- | --- |
| `license`, `projectStatus`, copyright and 2FA criteria | [Blocking conditions](#blocking-conditions) |
| `firstReleaseDate`, `totalCommits` | [Track record](#track-record) |
| `maintainerContinuity`, `committers`, `projectLeadPublicProfile` | [Continuity](#continuity-bus-factor) |
| `githubStars`, `contributorCount`, `nugetPackages` | [Adoption](#adoption) |
| `eligibilityCriteria` and the four evidence URLs, `cla`, `governanceModel` | [Operational hygiene](#operational-hygiene) |

A form with blank or contradicted fields could go back to the applicant rather than the evaluator filling the gaps. A field the repository contradicts would be treated as the applicant's answer being wrong, not as new information.

The lowest dimension would cap the level. Under this approach, a project with excellent adoption and a 5-week history would still be Pre-Seed.

### Track record

Suggested thresholds:

| Age since first public commit | Ceiling |
| --- | --- |
| Under 6 months | Pre-Seed |
| 6-18 months | Seed |
| Over 18 months | Member |

Age would run from first public commit, not repository creation, and it would be the one date the evaluator confirms against the repository rather than taking `firstReleaseDate` at face value. An application filed within 30 days of the repository going public could be treated as Pre-Seed by default.

### Continuity (bus factor)

| Maintainer situation | Ceiling |
| --- | --- |
| Sole maintainer, no succession plan | Seed |
| Sole maintainer with a named successor or an active org | Member, flagged |
| Two or more maintainers with merge rights in the last 6 months | Member |

A single maintainer need not be a reason to decline. What matters is whether anything happens to the project if that person stops. Seed may be a better fit for a project that would stall.

### Adoption

| Signal | Ceiling |
| --- | --- |
| No tagged release, or no package published | Pre-Seed |
| Released, but usage is not distinguishable from the maintainer's own CI | Seed |
| Sustained external usage over at least two release cycles | Member |

This deliberately avoids a download number. A niche library at 8,000 downloads can be more adopted than a template at 60,000. The evaluator would write one sentence on whether the usage is real and name the evidence: download curve shape, external issues and PRs, downstream dependents, third-party writeups or conference mentions. Whether to have a floor anyway is an open question (question 1).

### Operational hygiene

One option is to split the 17 eligibility criteria into two groups.

Load-bearing criteria, expected at Member level and allowed to stay open at Seed: a CLA mechanism, SECURITY.md, an issue tracker with maintainer responses, a public communication channel, documentation sufficient to use the project, dependency licenses cleared.

Onboarding items, allowed to stay open at either level and tracked as conditions: code signing, Source Link, reproducible build, discoverability metadata, home page.

A project failing load-bearing criteria could be capped at Seed until it fixes them. A project failing only onboarding items could be a Member under [Conditional Acceptance](project-levels.md#conditional-acceptance).

Self-attestation probably shouldn't count on its own. Each eligibility checkbox on the form would need an evidence URL next to it.

---

## Who could decide what

| Decision | Suggested owner |
| --- | --- |
| Blocking condition | Evaluator, confirmed by one other member, recorded in the notes |
| Decline after an unresolved blocking condition | Committee vote |
| Level assignment | Committee vote at the monthly meeting |
| Conditional Acceptance conditions | Evaluator drafts, committee approves |
| Seed 6-month review outcome | Committee vote, on the mentor's delta snapshot |
| Member health check | Reviewer, escalated to the committee only if it fails |
| Cooling-off waiver | Committee, with a stated reason in the notes |

Quorum has never been defined in the meeting notes. If level assignment becomes a vote, it would need defining (question 2).

---

## Recording it

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

## Open questions for the committee

1. Adoption deliberately avoids a number. Do we want a stated adoption floor (total downloads, external contributors, dependents) so borderline calls stay consistent between evaluators, accepting that any number will be wrong for some category of project?
2. What is quorum for a level vote, and can an evaluator vote on their own evaluation?
3. Transfers and sunsets. A Microsoft handover arrives with maturity but often without a maintainer. Does it enter at Member on its metrics, or at Seed until continuity is proven under new ownership? One reading is Seed, since continuity is the failing dimension and the one that decides whether the project survives.
4. Is 90 days the right window before a blocked application with a silent maintainer is closed?
