# VoyagerOS product overview

## Product statement

VoyagerOS is an in-development native Windows desktop companion. It explores a focused overlay for desktop actions, navigation, search, and contextual tools while preserving Windows as the operating system. It is not a replacement operating system, Windows Explorer, or the taskbar.

## Problem framing and vision

**Design hypothesis:** common desktop actions may be easier to reach when navigation, search, and contextual actions share a consistent native surface. This remains a hypothesis. No interviews, user research, adoption, conversion, or productivity measurements are claimed.

The product vision is a purposeful desktop layer that feels coherent with VoyagerOS's visual identity and predictable within Windows.

## Intended audience and value

The intended audience is people evaluating a more direct desktop workflow and testers who can provide reproducible Windows feedback. The intended benefit is shorter paths to app and search actions while retaining the existing Windows environment. This value has not yet been measured with users.

## Product boundary

VoyagerOS is an application-layer desktop experience. Windows continues to provide the operating system, desktop session, application model, and system services. VoyagerOS does not claim to replace Windows or provide a separate operating system.

The public repository is for product documentation, approved distribution artifacts, and feedback. The development source remains in the owner's private repository. No open-source license or redistribution terms are declared here.

## Experience areas

| Area | Development capability | Current evidence |
|---|---|---|
| Desktop | Native desktop surface, icon interaction, and rectangular selection | Source repair and automated regression coverage exist; release-candidate physical QA is pending |
| Dock | Dark native Dock and pointer-driven magnification | Controller automation exists; visual acceptance is pending |
| Start and Spotlight | Gesture arbitration, search controller, and direct-answer logic | Search logic has automated verification; physical surface acceptance is pending |
| Aurora | Contextual push-to-talk with native Windows speech and audio integration | Wired source and automated contracts exist; microphone and target-app QA is pending |
| QuickLook | Native preview service and lifecycle management | Integration exists; visible-window QA is pending |
| Settings and personalization | Native Win32 settings and persistence | Automated contracts exist; a current privacy-reviewed product screenshot is not available |
| Window management | Native host-window styles, hit testing, and message routing | Automated policy contracts exist; broader physical and multi-monitor acceptance remains open |

The [feature matrix](FEATURE_MATRIX.md) assigns the approved status labels and defines their scope.

## Product principles evidenced in the current work

1. **Complement Windows:** preserve the familiar desktop and system services.
2. **Preserve identity:** retain the established dark Dock material and original VoyagerOS artwork.
3. **Treat stability as product work:** the rectangular-selection crash was reproduced in the older private-alpha build, repaired in development source, and covered by a focused regression test.
4. **Separate component tests from acceptance:** automation is evidence for specific contracts, not proof of complete user-facing behavior.
5. **Release only one attributable package:** version, installer, runtime files, identity, integrity data, and notes must refer to the same candidate.

## Current release state

The public version is unassigned. A local 0.2.25 installer candidate exists, but it is marked PRIVATE_ALPHA, unsigned, built from a modified worktree, and has not completed physical acceptance or distribution review. It is not a public download.

For the latest checks, see the [release preflight](RELEASE_PREFLIGHT_2026-11-20.md) and [known limitations](KNOWN_LIMITATIONS.md).
