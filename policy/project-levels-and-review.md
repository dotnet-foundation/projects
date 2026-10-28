# .NET Foundation Project Levels

**Status:** Draft. Not yet adopted. The levels, thresholds and time windows below are proposals and may change.

This page explains what level a project could join the .NET Foundation at, what each level would include, and when a project would be looked at again.

---

## The levels

| Level | What it would mean | Listed on the Foundation site | Next review |
| --- | --- | --- | --- |
| **Blocked** | Evaluation is paused on a fixable problem | No | When you tell us it's fixed |
| **Pre-Seed** | Not accepted yet, usually because the project is too new or has little outside use | No | None. You can reapply after about 6 months |
| **Seed** | Accepted at a limited level, with a committee mentor | Possibly, marked Seed | Committee review at 6 months |
| **Conditional** | Accepted as a Member, with a short list of open items to close | Yes | Check at around 90 days |
| **Member** | Full Foundation project | Yes | Light health check every 12 months |
| **Declined** | A blocking problem the applicant has chosen not to fix | No | You could reapply after a cooling-off, suggested at 12 months |

---

## What each level could include

| | Pre-Seed | Seed | Member |
| --- | --- | --- | --- |
| Listing on dotnetfoundation.org | - | Possibly, marked Seed | Yes |
| A named committee mentor | - | Yes | - |
| CLA infrastructure and governance templates | - | Yes | Yes |
| Community promotion (newsletter, social, standups) | - | Yes | Yes |
| Code signing certificates | - | - | Yes |
| Trademark and IP handling | - | - | Yes |
| Funds, grants, infrastructure credits | - | - | Yes |
| Foundation logo as a project badge | - | `Seed` wording only | Yes |

Seed would hold back the expensive and hard-to-reverse services until the project has a track record inside the Foundation.

---

## Problems that pause an application

Any of these would pause the evaluation until it's fixed. None of them is a judgement on the project, and you can fix every one of them.

| Problem | How you could fix it |
| --- | --- |
| License is not OSI-approved, or is one the Foundation cannot accept | Relicense, with sign-off from every copyright holder |
| Name conflict, including org or package names that suggest Microsoft or Foundation endorsement | Rename, or provide written permission |
| Repository is archived, or described as a showcase, reference or experiment | Un-archive and state in writing that you intend to maintain it, or withdraw |
| Copyright ownership not confirmed, or the origin of forked, generated or translated code unclear | Confirm in writing, and document where derived code came from and its license |
| No commits in the 6 months before evaluation, and no reply from the maintainer | Reply, state your plans, and resume work |
| Repository is not public, or 2FA is not enabled on the org | Make it public and enable 2FA |

Once you show the fix, evaluation would restart on your current numbers. If we don't hear from you for a long time (suggested 90 days), the issue may be closed. You can reapply at any time.

A project would only be **Declined** if the problem can't be solved: the applicant won't fix it, the code's origin can't be established, or the same problem comes back on a third application.

---

## How the level could be decided

The proposal is to score four things from your application, each out of 100, then combine them.

| Factor | Weight | Low | Middle | High |
| --- | --- | --- | --- | --- |
| Real use | 35% | No release on NuGet | Released, little outside use | Used by others across 2+ releases (downloads, dependents, external issues or PRs) |
| Maintainers | 25% | One, no backup | One with a named successor, or backed by a company | Two or more who merged something in the last 6 months |
| Age | 25% | Under 6 months since first public commit | 6-18 months | Over 18 months |
| Stars | 15% | Under 100 | 100-1,000 | Over 1,000 |

| Score | Suggested level |
| --- | --- |
| 0-39 | Pre-Seed |
| 40-69 | Seed |
| 70-100 | Member |

A few notes:

- A repository under 6 months old would probably not go above Seed, whatever it scores.
- The evaluator could move one factor up or down a band and explain why in writing. A niche library with modest downloads can matter more than a popular template.
- The score would inform the committee's decision, not replace it.
- Age counts from your first public commit, not from when the repository was created.

**Quick fixes would not lower your score.** A CLA, SECURITY.md, code signing setup, Source Link, docs and package metadata can usually be sorted out in days. A project that scores as Member with some of these open could be accepted as **Conditional**, with about 90 days to close them. A Seed project would get them as its to-do list for the 6-month review.

---

## After the decision

**Pre-Seed.** You would get a written outcome naming the gap, a list of concrete things that would change the result, and a date after which you can reapply. A reapplication would need to show, item by item, what changed, with links. Applications filed before the date, or ones that repeat the original, may be closed without review.

**Seed.** Your mentor would bring your project's numbers to the committee at 6 months: commits, contributors, releases and downloads, then and now. The likely outcomes are promotion to Member, one more 6-month term, or a return to Pre-Seed. The suggested maximum at Seed is 12 months. If the committee misses your review date, it would move to the next meeting and nothing would change by default.

**Conditional.** If the open items aren't closed in time and we haven't heard from you, the project could move to Seed. If you're working on them and have a plan, an extension could be granted. Code signing would wait until the core items are done.

**Member.** Once a year, someone would check that the project is still active, still licensed as declared, and has a reachable maintainer. If something has slipped, you'd get a written notice and time to fix it before anything changes.

---

## Questions

Open an issue in [dotnet-foundation/projects](https://github.com/dotnet-foundation/projects/issues) or ask your committee mentor.
