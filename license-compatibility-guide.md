# License Compatibility Guide

This guide provides detailed information on license compatibility requirements for .NET Foundation projects, including both current member projects and prospective applicants.

## Compatible Licenses

The .NET Foundation accepts projects that use permissive open source licenses. Any permissive license from the [Open Source Initiative (OSI)](https://opensource.org/) approved list is acceptable.

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

## Incompatible Licenses

The Foundation does not accept projects using copyleft licenses. These include:

- GPL (GNU General Public License) - any version
- AGPL (GNU Affero General Public License)
- RPL (Reciprocal Public License)
- MPL (Mozilla Public License) in some contexts
- Other licenses with strong copyleft provisions

**Why copyleft licenses aren't compatible:** Copyleft licenses require derivative works to be licensed under the same terms, which can be less attractive to corporate users and doesn't align with the Foundation's goal of broad ecosystem compatibility.

The .NET community has a significantly higher proportion of enterprise and corporate users compared to many other open source ecosystems. These organizations often have strict legal requirements around license compatibility and derivative works. Permissive licenses provide the flexibility these users need, which is why they're fundamental to the Foundation's mission of supporting the .NET ecosystem effectively.

## Supported Business Models

The Foundation supports various business models for member projects:

### 1. Dual Licensing

Projects may offer their code under two licenses simultaneously:

- One permissive OSI-approved license (for the open source community)
- One commercial license (offering additional warranties, guarantees, or terms)

The Foundation operates on a per-repository basis. As long as the source code is available under a permissive license, dual licensing is acceptable.

### 2. Commercial Services

Projects may offer commercial services built around their open source code, including:

- Premium support packages
- Consulting services
- Training and certification
- Managed hosting
- Enterprise warranties and SLAs

The source code must remain free and open under a permissive license. Commercial services built around the code are acceptable.

### 3. Sponsorship and Funding

Projects are encouraged to use [GitHub Sponsors](https://github.com/sponsors) and other funding platforms to build sustainable support for maintainers.

### 4. Company Formation and Commercial Editions

Projects may:

- Establish a company around the project
- Offer commercial editions with additional features
- Provide paid support tiers
- Maintain proprietary premium packages (provided the core remains under a permissive license)

## Core Licensing Principle

The Foundation's core requirement is that project source code must be freely available under a permissive open source license. Premium support, commercial editions, and value-added services are compatible with Foundation membership provided the core source code remains under a permissive license.

## Guidelines for Current and Prospective Maintainers

.NET Foundation project maintainers have flexibility in how they structure their projects and business models:

### Permitted Activities:

- Implement dual licensing (permissive + commercial)
- Form a company around the project
- Charge for premium support and services
- Create paid tiers and enterprise offerings
- Use GitHub Sponsors or other funding platforms
- Maintain proprietary premium packages (provided core remains under a permissive license)
- Offer commercial warranties and guarantees

### Prohibited Activities:

- Switch to a copyleft license (GPL, AGPL, RPL, etc.)
- Make mandatory dependencies use copyleft licenses

**Why copyleft licenses aren't compatible:**

Copyleft licenses require derivative works to be licensed under the same terms, which can be less attractive to corporate users and doesn't align with the Foundation's goal of broad ecosystem compatibility.

The .NET community has a significantly higher proportion of enterprise and corporate users compared to many other open source ecosystems. These organizations often have strict legal requirements around license compatibility and derivative works. Permissive licenses provide the flexibility these users need, which is why they're fundamental to the Foundation's mission of supporting the .NET ecosystem effectively.

## Questions or Feedback

If you have questions about license compatibility or need clarification on any of these guidelines, please [open an issue](https://github.com/dotnet-foundation/projects/issues) in this repository.

The Foundation supports sustainable business models around open source projects. Commercial services, paid support, and business development around open source work are compatible with Foundation membership requirements.
