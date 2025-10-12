# License Compatibility Guide

## Understanding What's Compatible (and What's Not)

## What Licenses ARE Compatible

The .NET Foundation accepts projects that use permissive open source licenses. We automatically approve any permissive license from the [Open Source Initiative (OSI)](https://opensource.org/) approved list.

Examples of compatible permissive licenses:

- MIT License
- Apache License 2.0
- BSD licenses (2-clause, 3-clause)
- ISC License

**Key requirements:**

- Your main codebase must use a permissive OSI-approved license
- Mandatory dependencies must also use permissive licenses (with exceptions for platform-specific requirements like .NET Framework or hardware-specific libraries where no open source alternative exists)
- Committers must be bound by a Contributor License Agreement (CLA) or willing to embrace the .NET Foundation's CLA
- Copyright ownership must be clearly defined and documented

## What Licenses Are NOT Compatible

The Foundation does not accept projects using copyleft licenses. These include:

- GPL (GNU General Public License) - any version
- AGPL (GNU Affero General Public License)
- RPL (Reciprocal Public License)
- MPL (Mozilla Public License) in some contexts
- Other licenses with strong copyleft provisions

**Why copyleft licenses aren't compatible:** Copyleft licenses require derivative works to be licensed under the same terms, which can be less attractive to corporate users and doesn't align with the Foundation's goal of broad ecosystem compatibility.

The .NET community has a significantly higher proportion of enterprise and corporate users compared to many other open source ecosystems. These organizations often have strict legal requirements around license compatibility and derivative works. Permissive licenses provide the flexibility these users need, which is why they're fundamental to the Foundation's mission of supporting the .NET ecosystem effectively.

## Business Models We Support

### The Foundation DOES Support These Business Strategies:

#### 1. Dual Licensing

You can offer your project under TWO licenses simultaneously:

- One permissive OSI-approved license (for the open source community)
- One commercial license (offering additional warranties, guarantees, or terms)

This is perfectly acceptable! The Foundation operates on a per-repository basis, so as long as the source code is available under a permissive license, you're good to go.

#### 2. Commercial Services Around Open Source

- Premium support packages
- Consulting services
- Training and certification
- Managed hosting
- Enterprise warranties and SLAs

**Important:** The source code must remain free and open, but services built around it don't have to be.

#### 3. [GitHub Sponsors](https://github.com/sponsors)

We actively encourage projects to use GitHub Sponsors to build sustainable funding for maintainers.

#### 4. Company Formation

You can:

- Set up a company around your project
- Offer commercial editions with additional features
- Provide paid support tiers
- Keep premium packages proprietary (as long as the core remains permissive)

### Our Core Principle

**"As long as the source is free, that is our condition."**

You don't have to make everything available as free packages. Premium support, commercial editions, and value-added services are all compatible with Foundation membership.

## For Maintainers: Your Options

As a .NET Foundation project maintainer, you have flexibility:

### You CAN:

- Implement dual licensing (permissive + commercial)
- Form a company around your project
- Charge for premium support and services
- Create paid tiers and enterprise offerings
- Use GitHub Sponsors or other funding platforms
- Keep some packages proprietary (as long as core is permissive)
- Offer commercial warranties and guarantees

### You CANNOT:

- Switch to a copyleft license (GPL, AGPL, RPL, etc.)
- Make mandatory dependencies use copyleft licenses

**Why copyleft licenses aren't compatible:**

Copyleft licenses require derivative works to be licensed under the same terms, which can be less attractive to corporate users and doesn't align with the Foundation's goal of broad ecosystem compatibility.

The .NET community has a significantly higher proportion of enterprise and corporate users compared to many other open source ecosystems. These organizations often have strict legal requirements around license compatibility and derivative works. Permissive licenses provide the flexibility these users need, which is why they're fundamental to the Foundation's mission of supporting the .NET ecosystem effectively.

## Questions?

Feel free to contact us at contact@dotnetfoundation.org, join our [Discord](https://discord.gg/dotnet-foundation) or interact with us on social media.

**Remember: We want you to succeed sustainably!** Building commercial services, offering paid support, and creating business models around your open source work is not just allowed—it's encouraged.
