# CLA Troubleshooting Guide

This guide provides step-by-step procedures for investigating and resolving issues with the Contributor License Agreement (CLA) bot used by .NET Foundation projects.

## Overview

The .NET Foundation uses an automated CLA bot to verify that contributors have signed the required Contributor License Agreement before their pull requests can be merged. This bot is managed by Microsoft and integrated with GitHub.

## Common Issues

### Inconsistent CLA Bot Reports

Sometimes the CLA bot may report different statuses for the same contributor across multiple pull requests. This can happen for several reasons:

1. **Timing Issues**: The contributor signed the CLA between opening different PRs
2. **Email Mismatch**: The contributor used different email addresses for different commits
3. **Bot Synchronization**: The CLA bot database is out of sync with the actual signatures
4. **Account Association**: The contributor's GitHub account is not properly associated with their CLA signature

## Investigation Steps

When you encounter inconsistent CLA bot reports, follow these steps to investigate:

### Step 1: Verify Contributor Identity

1. **Check the commit author information** in both PRs:
   ```bash
   # View commit details for a specific PR
   git log --format="%H %ae %an" origin/pull/PULL_NUMBER/head
   ```

2. **Compare email addresses** used in commits across the different PRs:
   - Are they using the same email address?
   - Is the email address associated with their GitHub account?
   - Do they have multiple email addresses configured?

3. **Check GitHub profile**:
   - Visit the contributor's GitHub profile
   - Look at their configured email addresses (if public)
   - Check if they have verified their email addresses

### Step 2: Check CLA Bot Comments

1. **Review bot comments** on both pull requests:
   - Look for the exact message from the CLA bot
   - Note any differences in the messages
   - Check if the bot mentions specific issues (e.g., "email not found")

2. **Look for CLA signature links**:
   - The bot typically provides a link to sign the CLA
   - Check if this link was followed by the contributor

### Step 3: Verify CLA Signature Status

Since the CLA bot is managed internally by Microsoft, project maintainers do not have direct access to the CLA database. To verify a contributor's CLA status:

1. **Contact .NET Foundation Support**:
   - [Submit a Project Support Request](https://github.com/dotnet-foundation/projects/issues/new?assignees=ChrisSfanos&labels=project+support%2Ctriage&template=project-support-request.yml&title=%5BProject+Support%5D%3A+CLA+Status+Investigation)
   - Include:
     - Project name
     - Contributor's GitHub username
     - Links to all affected pull requests
     - Details about the inconsistency

2. **Email Contact**:
   - For confidential matters, email: contact@dotnetfoundation.org
   - Include the same information as above

3. **Discord Channel**:
   - Join the [.NET Foundation Discord](https://discord.gg/dotnet-foundation)
   - Post in the `#projects-support` channel
   - Provide the GitHub issue link for tracking

### Step 4: Common Solutions

While waiting for support team investigation, you can try these potential solutions:

1. **Ask the contributor to re-trigger the CLA bot**:
   ```
   @contributor Can you please comment `/cla` on this PR to re-trigger the CLA bot check?
   ```
   Or ask them to add a trivial commit (e.g., whitespace change) to force a re-check.

2. **Verify email configuration**:
   - Ask the contributor to ensure their commit email matches their CLA signature email
   - They can check their git config: `git config user.email`
   - They may need to amend commits if the email is wrong

3. **Check for GitHub account linking**:
   - The contributor should ensure their GitHub account is properly linked to the email they used for the CLA
   - They can verify this in GitHub Settings > Emails

4. **Re-sign the CLA** (if necessary):
   - If all else fails, the contributor may need to sign the CLA again
   - The CLA bot comment usually includes a link to the CLA signing page

## Escalation Process

If the issue cannot be resolved through the steps above:

1. **Project Support Team** (@ChrisSfanos and team):
   - Has access to internal Microsoft resources
   - Can directly investigate CLA database issues
   - Can coordinate with the CLA bot team if needed

2. **Timeline**:
   - Support requests are typically reviewed within a few business days
   - Complex CLA issues may require coordination with Microsoft Legal
   - Keep the contributor informed of progress

3. **Interim Workarounds**:
   - While investigating, maintain communication with the contributor
   - Keep the PR open and mark it as "waiting for CLA verification"
   - Document the issue in the PR comments for transparency

## Best Practices for Maintainers

1. **Be Patient and Professional**: CLA issues can be frustrating, but they're usually resolvable.

2. **Document Everything**: Keep clear records of what you've checked and attempted.

3. **Communicate Clearly**: Keep contributors informed about what's happening and what's needed from them.

4. **Don't Merge Without CLA**: Even if you trust the contributor, always wait for proper CLA verification before merging.

5. **Report Patterns**: If you notice recurring issues with the CLA bot, report them to the support team so they can be addressed systematically.

## Technical Details

### How the CLA Bot Works

1. **Trigger**: The bot is triggered automatically when:
   - A new PR is opened
   - New commits are pushed to an existing PR
   - Someone comments `/cla` on the PR

2. **Verification**: The bot checks:
   - The email addresses of all commit authors in the PR
   - Whether those emails have associated CLA signatures in the database
   - Whether the signatures are current and valid

3. **Status Update**: The bot posts a comment indicating:
   - ✅ All contributors have signed the CLA
   - ❌ One or more contributors need to sign the CLA
   - Links to sign the CLA if needed

### Known Limitations

1. **Email Matching**: The system relies on exact email matches. Case sensitivity and whitespace can cause issues.

2. **GitHub Integration**: The bot depends on GitHub's commit author information, which can be configured incorrectly.

3. **Caching**: There may be delays in status updates due to caching in various systems.

4. **Multiple Accounts**: Contributors with multiple GitHub accounts or email addresses may encounter issues.

## Additional Resources

- [.NET Foundation CLA Information](https://github.com/dotnet-foundation/projects/blob/main/new-projects.md#signing-the-cla)
- [Project Support Request Template](https://github.com/dotnet-foundation/projects/issues/new?assignees=ChrisSfanos&labels=project+support%2Ctriage&template=project-support-request.yml)
- [.NET Foundation Discord](https://discord.gg/dotnet-foundation)
- Email: contact@dotnetfoundation.org

## Questions or Feedback

If you have suggestions for improving this guide or encounter issues not covered here, please [open an issue](https://github.com/dotnet-foundation/projects/issues) in this repository.
