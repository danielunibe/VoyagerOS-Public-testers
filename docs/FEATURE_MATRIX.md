# Feature matrix

This matrix describes the current development source and its evidence. It is not a claim that a public build is available. Status labels follow the required scope:

- **VERIFIED** — automated evidence verifies the specific scope stated in the row; it does not imply full product acceptance.
- **IMPLEMENTED_UNVERIFIED** — code is present or wired into the active shell, but required physical, visual, device, or release-candidate checks remain open.
- **EXPERIMENTAL** — available only as an opt-in or exploratory development path.
- **PLANNED** — intended work with no verified current implementation.
- **UNAVAILABLE** — no current user-facing capability or public artifact exists.

| Capability | Status | Evidence and remaining checks |
|---|---|---|
| Desktop and rectangular selection | IMPLEMENTED_UNVERIFIED | Development source includes a repair and a focused regression test; current candidate has not completed physical mouse QA. The installed private-alpha 0.2.24 build is known to crash on this path. |
| Dock and pointer magnification | IMPLEMENTED_UNVERIFIED | Controller and layout automation exist; visual acceptance on the exact candidate remains open. |
| Start gestures and Windows-key path | IMPLEMENTED_UNVERIFIED | Tap, double-tap, and hold policies are wired and covered by automated contracts; physical key and focus-continuity checks remain open. |
| Spotlight search controller | VERIFIED | Automated tests verify the search controller and direct-answer logic only. Full visible-surface acceptance remains open. |
| Aurora push-to-talk dictation | IMPLEMENTED_UNVERIFIED | Source is wired to Windows speech and audio components; real microphone, privacy settings, target applications, and language requirements remain unverified. |
| Overlay InputRouter | IMPLEMENTED_UNVERIFIED | Region-binding contracts are present; visible-window hit testing needs acceptance. |
| QuickLook native preview lifecycle | IMPLEMENTED_UNVERIFIED | Native preview and teardown integration exist; visible-window and file-type acceptance remain open. |
| Native Settings and persistence contracts | VERIFIED | Automated contracts verify the settings service and persistence scope. Current visual/product acceptance is not claimed. |
| Native window styles and message dispatch | VERIFIED | Automated policy and dispatch contracts are verified; broader display, focus, and multi-monitor behavior remains open. |
| Personalization experience | IMPLEMENTED_UNVERIFIED | Native settings support exists; full current-screen visual review and end-to-end persistence acceptance remain open. |
| Public installation package | UNAVAILABLE | A local 0.2.25 setup candidate exists, but it is PRIVATE_ALPHA, unsigned, from a modified worktree, and not approved for public distribution. |
| In-app automatic updater | UNAVAILABLE | No verified in-app update capability is available; updates are not automatic. |

The 0.2.25 candidate is traceable to the current modified worktree and its executable matches its identity record. That provenance does not clear the remaining distribution and manual QA gates. See [Known Limitations](KNOWN_LIMITATIONS.md) and the [release preflight](RELEASE_PREFLIGHT_2026-11-20.md).
