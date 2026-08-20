# Security Policy

This is the default policy for Cirth organization repositories that do not
publish their own `SECURITY.md`. A repository-specific policy takes precedence.

## Supported versions

Security fixes are developed on the current default branch of actively
maintained Cirth repositories and, when applicable, released for the latest
stable version or published package. Fixes are not normally backported to older
releases. Prereleases and archived repositories are not supported.

If you are unsure whether an affected version is supported, report the issue
privately anyway and include the exact version or commit.

## Reporting a vulnerability

Do not open a public issue, pull request, or discussion containing vulnerability
details, working exploits, credentials, private data, or information that would
make exploitation easier.

In the affected repository, open the **Security** tab and select **Report a
vulnerability**. This private GitHub channel is preferred when the button is
available.

If private vulnerability reporting is unavailable, email the Cirth maintainers
at [hello@ricpastori.com](mailto:hello@ricpastori.com) with a subject identifying
the affected repository. Do not send secrets, access tokens, real user data, or
unredacted private URLs.

A useful report includes:

- the affected repository and version or commit;
- the affected package, release, or published artifact, if applicable;
- the security impact and a realistic attack scenario;
- safe reproduction steps or a minimal proof of concept;
- relevant environment or browser details;
- any suggested mitigation;
- whether the issue has been disclosed elsewhere.

## Scope

A report is in scope when Cirth-controlled code, configuration, documentation,
or infrastructure creates or materially worsens the security issue. Examples
include:

- project source code and build scripts;
- official build, packaging, release, or deployment workflows;
- published packages, release archives, and their metadata or exports;
- unexpected differences between tagged source and an official published
  artifact;
- official installation or distribution instructions that create a concrete
  security risk.

For `@cirthcss/cirth`, this includes the SCSS-to-CSS build pipeline, compiled
`dist/` files, package exports, npm publication, and GitHub release artifacts.

### Dependency reports

Report a third-party dependency vulnerability privately when either of these is
true:

- the vulnerable behavior is reachable in the way a Cirth project actually
  uses the dependency;
- it could compromise a Cirth build, CI workflow, release credential, or
  official published artifact.

An advisory or scanner match against a package name and version is not enough on
its own. Include a plausible impact and exploit path for the affected Cirth
project.

The published `@cirthcss/cirth` package contains compiled CSS and currently
declares no runtime dependencies. Vulnerabilities in its development
dependencies are in scope only when they can affect Cirth's development, build,
or release process; consumers do not receive those tools as package runtime
dependencies.

A vulnerability in an unrelated application or package that happens to use
Cirth is out of scope unless Cirth's code, package, or official guidance causes
or materially worsens it.

Ordinary rendering defects, visual regressions, browser compatibility,
accessibility, performance, and documentation problems should normally be
reported through the public issue tracker. Report them privately only when they
have a concrete security impact.

Issues belonging entirely to GitHub, npm, browsers, CDNs, or unrelated upstream
dependencies should be reported to the responsible project. Cirth still accepts
a report when its own configuration or integration materially increases the
risk.

Do not test against systems or data you do not own or have permission to use.
Do not perform denial-of-service, destructive testing, social engineering, or
activity that could affect other users.

## What to expect

Maintainers will review actionable reports, may request more information, and
will coordinate any fix and disclosure they decide is appropriate. Please keep
sensitive details private until a resolution or disclosure plan has been
agreed.

Response times are best effort. This policy does not promise a response or
disclosure deadline, severity classification, fix, release, or continued support
for an affected version. Reporters may be credited if they want to be and if a
public disclosure is made.

Cirth does not currently operate a bug bounty program or promise payment for
reports. This policy is a reporting guide, not a security audit, certification,
or guarantee that Cirth projects are free of vulnerabilities.
