# VoyagerOS

**A native Windows desktop companion exploring a focused overlay, Dock, and contextual app and search interactions.**

VoyagerOS is an in-development native desktop experience for the existing Windows environment. It explores more direct ways to reach desktop actions while preserving Windows as the operating system. VoyagerOS is not a standalone operating system or a replacement for Windows Explorer or the taskbar.

The native runtime is built around Win32, Direct3D 12, DirectComposition, and a Rust core. Development work is kept in a private source repository; this public repository is for distribution, release notes, and tester feedback.

> **Public status: preparation.** No public download or release is available yet.

## Product status

- This repository currently has no public release or version tag.
- An earlier draft named **0.2.1** as a planned first release. That was a planning label, not a published or currently approved public version.
- The locally inspected **0.2.24** package is marked `PRIVATE_ALPHA`, is unsigned, and was built from a modified source tree. It is excluded from public distribution.
- The public version will be assigned from a verified `PUBLIC` package after its source, installer, requirements, and integrity checks are complete.
- No product screenshot is included in this preparation.

## Product direction

The development implementation includes a native desktop layer and a dark Dock. Search and Spotlight surfaces are being developed alongside Aurora dictation. These areas have not all completed the visual, interaction, and device checks needed for a public release.

See the [product overview](docs/PRODUCT_OVERVIEW.md), [product decisions](docs/PRODUCT_DECISIONS.md), and [roadmap](docs/ROADMAP.md) for scope and current validation gaps.

## Downloads

There is no public installer yet. When a candidate passes the release gates, downloads will appear on [GitHub Releases](https://github.com/danielunibe/VoyagerOS-Public-testers/releases), with version-matched installation instructions, SHA-256, and an accurate Authenticode status.

The current update path is manual through GitHub Releases. The application does not provide an in-app automatic updater.

## Requirements

Public Windows version, architecture, dependencies, and installation steps will be documented with the first verified public package. Do not use private-alpha builds as public downloads.

## Feedback

Use [GitHub Issues](https://github.com/danielunibe/VoyagerOS-Public-testers/issues/new/choose) to report a reproducible problem or suggest an improvement. Include only the details needed to understand the report. Remove names, file paths, notifications, and other personal information from optional evidence.

## Project boundary

This repository contains public product and distribution material. It does not mirror the private source tree, internal audit logs, user data, saves, or build directories. Release readiness and the current artifact inventory are summarized in the [public preflight](docs/RELEASE_PREFLIGHT_2026-11-20.md).
