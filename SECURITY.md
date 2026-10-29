# Security Policy

GPMP manages Group Policy information and can perform privileged operations in Active Directory. Please report suspected security vulnerabilities privately so they can be investigated without exposing affected installations.

## Supported Versions

Security fixes target the latest published GPMP release. Older releases do not have a separate security maintenance branch; upgrading may be required to receive a fix.

| Version or channel | Security maintenance |
| --- | --- |
| Latest published release | Best effort |
| Older releases | No dedicated security updates; upgrade to the latest release |
| Nightly builds and unpublished `main` snapshots | Development builds; no security support guarantee |

Where the latest release is a development or release-candidate build, it remains a pre-release. Security maintenance does not imply production readiness or a guarantee that the software is free of vulnerabilities.

This policy covers GPMP Core, project-maintained modules, launchers, installation and update scripts, and export functionality. Third-party components also follow their respective vendors' security policies.

## Reporting a Vulnerability

**Do not publish vulnerability details in public issues, discussions, pull requests, or attachments.**

Use [GitHub private vulnerability reporting](https://github.com/PScherling/Sensei/security/advisories/new): open the repository's **Security and quality** tab and select **Report a vulnerability**, when available.

If private reporting is unavailable, open a public issue titled **Security contact request** asking for a private reporting channel. Do not include affected endpoints, exploit details, logs, or sensitive configuration in that issue. Wait for a private channel before sharing the report.

### What to Include

- GPMP version, release channel, package profile, and relevant module versions.
- The affected component or operation and a description of the suspected vulnerability.
- Reproduction steps or a minimal proof of concept using a test environment.
- Expected and observed behavior, potential impact, and any required permissions or configuration.
- Relevant sanitized logs, screenshots, or dependency advisory identifiers.

Remove passwords, connection strings, tokens, account details, and other secrets. GPO reports, database exports, analysis packages, and screenshots can contain sensitive domain information; share only the minimum sanitized evidence needed. Do not upload a complete database backup or production report collection unless specifically requested through the private channel.

## Report Handling and Disclosure

Reports are handled on a best-effort basis. There is no guaranteed acknowledgment, update interval, or resolution deadline. Follow-up questions, investigation updates, and remediation discussions should remain in the private report or agreed private channel.

Accepted reports will be investigated and prioritized according to impact and exploitability. A resolution may include a code change, dependency update, mitigation, or upgrade guidance. When a report is declined or cannot be reproduced, the maintainer will aim to explain the decision and identify any additional evidence needed.

Please coordinate public disclosure with the maintainer to allow affected users time to update. Confirmed vulnerabilities may be documented through a GitHub security advisory and release notes. Reporter credit can be agreed during disclosure; anonymous reporting credit preferences will be respected.

## Responsible Testing

Test only systems you own or have explicit authorization to assess. Use an isolated test domain where possible. Avoid disrupting services, changing production GPOs, accessing other users' data, or testing third-party installations without permission.

Ordinary defects, feature requests, and usability issues without a security impact belong in the repository's public issue tracker.
