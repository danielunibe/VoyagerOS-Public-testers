<div align="center">
  <img src="assets/brand/voyager-icon.png" alt="VoyagerOS official space emblem" width="104">
  <h1>VoyagerOS</h1>
  <p><strong>A native Windows desktop companion for contextual navigation, search, and desktop actions.</strong></p>
  <p>IN DEVELOPMENT &nbsp;·&nbsp; WINDOWS &nbsp;·&nbsp; NO PUBLIC BUILD</p>
</div>

---

## Product preview

This repository does not yet include a current VoyagerOS interface screenshot. The image above is the official project emblem, not a screenshot. Older images available in the development archive show an earlier beta or QA fixtures, so they are not presented as current product evidence. The native desktop could not be captured in this review, and the project owner chose to continue without new captures.

The exact capture checklist for a future, privacy-reviewed gallery is in [assets/screenshots/README.md](assets/screenshots/README.md).

## What is VoyagerOS?

VoyagerOS is an in-development native desktop companion for Windows. It explores a focused overlay with desktop, Dock, Start, search, and contextual actions while Windows remains the host operating system. It is not a standalone operating system and does not replace Windows Explorer or the taskbar.

**Product hypothesis:** a consistent, native layer may make common desktop actions easier to reach without replacing familiar Windows workflows. This is a design hypothesis; no user research, adoption, or measured outcome is claimed here.

## Experience highlights

These describe development-source capabilities, not a downloadable product. See the [feature matrix](docs/FEATURE_MATRIX.md) for verification scope.

- **Desktop and selection** — native desktop interactions and rectangular selection. A source fix and focused regression test exist; physical interaction checks on the release candidate remain open.
- **Dock** — a dark native Dock with pointer-driven magnification. Controller tests exist; visual acceptance remains open.
- **Start and Spotlight** — gesture-driven entry and a search controller. Automated search logic is covered; real desktop interaction acceptance remains open.
- **Aurora** — contextual push-to-talk dictation wired to Windows speech and audio components. Microphone, permission, and target-app checks remain open.
- **QuickLook and Settings** — native preview lifecycle plus a native settings surface and persistence. The development contracts are covered to different extents; see the matrix before interpreting status.

## Product thinking

The current product decisions make the scope and trade-offs explicit: VoyagerOS complements Windows, keeps the existing visual identity, prioritizes a user-visible crash before release work, and requires evidence for the exact candidate. Automated component tests do not stand in for physical or visual acceptance.

Read the [product overview](docs/PRODUCT_OVERVIEW.md), [product decisions](docs/PRODUCT_DECISIONS.md), and [known limitations](docs/KNOWN_LIMITATIONS.md).

## Technical architecture

The active desktop shell is a C++20 Win32 application using Direct3D 12 and DirectComposition. Rust core and Windows-platform components connect to the native host through a defined ABI. Native window procedures and surface-specific policies route input to the desktop, Dock, Start and search, QuickLook, and settings.

See the [technical overview](docs/TECHNICAL_OVERVIEW.md) for the high-level component map and validation scope.

## Product evolution

- An earlier public-repository draft listed 0.2.1 as a planned first version. It was never published and is not the current version.
- The installed private-alpha 0.2.24 build had a confirmed crash during rectangular desktop selection.
- The current development source contains a repair and a focused regression test. A local 0.2.25 candidate matches its build identity and the current modified worktree, but remains marked PRIVATE_ALPHA, is unsigned, and has not completed physical release-candidate QA.
- The CMake project declaration is 0.2.0 while the local package, executable, build identity, and package manifest report 0.2.25. Their mapping is not reconciled; no public version is assigned.
- No public version, download, tag, or GitHub Release has been assigned.

The release evidence and exact blockers are in the [release preflight](docs/RELEASE_PREFLIGHT_2026-11-20.md).

## Roadmap

The immediate work is to produce a clean, approved source cut; verify installation and real desktop interaction on the exact candidate; complete device and surface QA; and publish clear requirements and integrity data only after those gates pass.

See the [roadmap](docs/ROADMAP.md).

## Download and installation

**There is no public download yet.** The [GitHub Releases page](https://github.com/danielunibe/VoyagerOS-Public-testers/releases) is the intended distribution channel and currently has no release. The local 0.2.25 setup candidate is not offered because it is private-alpha, unsigned, built from a modified worktree, and still lacks release-candidate validation and confirmed distribution terms.

No minimum Windows version or public dependency list is claimed until they are tested against an approved package. VoyagerOS has no verified in-app automatic updater; future updates would be manual through Releases.

## Known limitations

- The installed private-alpha 0.2.24 build has the confirmed rectangular-selection crash described above.
- The 0.2.25 candidate has not been exercised through the physical desktop checks required for release.
- Aurora microphone and target-application behavior, Start gestures, Dock visuals, QuickLook presentation, and multi-monitor behavior still need real Windows acceptance.
- No current product screenshots, public installer, public version, or release is available.
- The public repository has no license file; distribution terms have not been established.

Full details are in [Known Limitations](docs/KNOWN_LIMITATIONS.md).

## Feedback

Use [GitHub Issues](https://github.com/danielunibe/VoyagerOS-Public-testers/issues/new/choose) to report a reproducible issue or suggest a product improvement. Remove names, file paths, notifications, and other personal information from evidence before attaching it.

## Project ownership

Project owner: [@danielunibe](https://github.com/danielunibe). No broader team, commercial result, or user-research outcome is claimed. Development source remains private; this repository contains public product documentation, approved brand material, release information, and tester feedback.

## Navigate

[Product overview](docs/PRODUCT_OVERVIEW.md) · [Decisions](docs/PRODUCT_DECISIONS.md) · [Technical overview](docs/TECHNICAL_OVERVIEW.md) · [Feature matrix](docs/FEATURE_MATRIX.md) · [Roadmap](docs/ROADMAP.md) · [Known limitations](docs/KNOWN_LIMITATIONS.md) · [Release preflight](docs/RELEASE_PREFLIGHT_2026-11-20.md) · [Distribution guide](docs/DISTRIBUCION_Y_ACTUALIZACIONES.md) · [Changelog](CHANGELOG.md) · [Recovery report](VOYAGEROS_PUBLIC_RELEASE_RECOVERY_REPORT.md)
