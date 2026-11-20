# Known limitations

These limitations are based on current repository and artifact evidence. They describe the development build and local candidates, not a supported public release.

## Release blockers

- **No public version or download:** the Releases page has no published release. The local setup candidate is marked PRIVATE_ALPHA.
- **Modified source cut:** the 0.2.25 build identity matches the current modified worktree and its executable, but that worktree is not a clean, owner-approved public source cut.
- **Unresolved version mapping:** CMake declares project version 0.2.0, while the local executable, installer, build identity, and package manifest report 0.2.25. The public version remains unassigned until the owner documents the version source of truth.
- **Installer integrity record is incomplete:** the identity record covers the executable and runtime artifacts; the setup executable itself is not listed in that record.
- **Unsigned files:** Authenticode reports the 0.2.25 executable and setup candidate as unsigned.
- **Distribution terms:** the public repository has no license file and no redistribution terms have been established.
- **No exact-candidate installation acceptance:** installation, launch, uninstall, and recovery have not been verified on the local 0.2.25 setup candidate.
- **No physical/visual acceptance:** the candidate has not completed physical desktop, visual, or multi-monitor QA.

## Confirmed desktop selection issue in the older build

The installed private-alpha 0.2.24 executable was confirmed to crash during rectangular desktop selection when the selection crossed a physical folder. Development source contains a repair and regression coverage. The focused desktop-selection test passed a fresh 1/1 run in this review. The 0.2.25 build identity and executable match the current worktree, which contains the repair, but the candidate has not been run through physical mouse acceptance. The issue is therefore not declared fixed in a released or user-accepted build.

## Feature-specific validation gaps

- **Aurora:** real microphone, Windows privacy settings, supported speech configuration, target application, and non-editable/elevated target behavior.
- **Start:** physical Windows-key and pill gestures, timing, focus continuity, and activation-loss behavior.
- **Dock and InputRouter:** visual acceptance, hit testing, pointer boundaries, and interaction in visible surfaces.
- **Spotlight and QuickLook:** visible layout, keyboard and pointer flow, focus behavior, and preview compatibility.
- **Settings and personalization:** current end-to-end visual acceptance and persistence across a fresh install.
- **Display support:** minimum Windows version, DPI range, multi-monitor support, and recovery across display changes have not been finalized.

## Images and project status

No current product screenshot is included. The official brand emblem is not a product screenshot. Older beta images and QA fixture captures were excluded because they do not prove the current interface.

There is no verified in-app updater. No open-source status or redistribution license is claimed.
