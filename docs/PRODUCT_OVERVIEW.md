# VoyagerOS product overview

## Product statement

VoyagerOS is an in-development native Windows desktop experience. It explores a focused overlay, a Dock, and app and search workflows that coexist with the existing Windows desktop. It is not a standalone operating system and does not replace Windows Explorer or the taskbar.

## Product problem and vision

Desktop actions such as reaching an app, a search surface, or a contextual tool can involve switching between several Windows surfaces. VoyagerOS explores whether a coherent native layer can make those interactions feel more direct while keeping the familiar Windows environment available.

The vision is a purposeful, responsive desktop companion with a consistent visual identity and predictable Windows behavior.

## Approach

The current product implementation uses a Win32 host, Direct3D 12, DirectComposition, and a Rust core. The product direction preserves the Windows avatar, original project artwork, and dark Dock material. The public repository is a distribution and feedback channel; development source remains private.

## Capability and validation status

| Area | Development status | Public-release validation |
|---|---|---|
| Native desktop overlay and Dock | Present in the development implementation | Visual and physical interaction acceptance is still open; no public capture is included |
| Search and Spotlight surfaces | Under active development | Not approved as a released capability |
| Aurora dictation | Integrated development work exists | Real microphone and target-application checks remain open |
| Public installation and updates | Manual GitHub Releases is the planned distribution path | No public installer, requirements matrix, or published version is available |

The statuses above distinguish development work from user-facing release acceptance. Passing code or synthetic tests alone does not establish that a Windows interaction is ready for testers.

## Scope boundaries

VoyagerOS is a Windows desktop companion, not a replacement operating system. No universal Windows compatibility, stable-release status, automatic updating, or user-research outcome is claimed here.

## Current state

The repository is preparing a public tester experience. The public version is unassigned until an exact-source `PUBLIC` package passes its release checks. The [distribution guide](DISTRIBUCION_Y_ACTUALIZACIONES.md) explains the release path; the [roadmap](ROADMAP.md) tracks the open validation work.
