# Public release preflight — 2026-11-20

## Decision

**Public documentation: ready to publish. Binary release: blocked.**

The public repository's main branch had no release or version tag at the start of this review. The earlier draft's 0.2.1 label was never published and is not the current public version.

## Candidate evidence

| Item | Observed state | Distribution decision |
|---|---|---|
| Installed private-alpha 0.2.24 | Windows executable; unsigned; a crash during rectangular desktop selection was reproduced | Do not distribute |
| Local 0.2.25 setup candidate | Version 0.2.25; Windows x64; unsigned; channel PRIVATE_ALPHA | Do not publish |
| 0.2.25 build identity | Source head, source fingerprint, source count, executable version, and executable hash match the current modified worktree and candidate. The build record includes 230/230 automatic CTest results. | Provenance is traceable to a modified worktree, not a clean public source cut |
| Package contents | Package manifest matches the listed runtime executable and Rust modules; setup executable itself is not recorded in the identity artifact list | End-to-end installer integrity is incomplete |
| Focused crash regression | Fresh run of the desktop-selection regression test passed 1/1; prior recovery record reports 44 assertions for that test | Source-level evidence only; physical mouse QA on the candidate remains open |
| Signature | Authenticode reports the 0.2.25 executable and setup candidate as unsigned | Signing decision and distribution policy remain open |
| Requirements and install behavior | No public Windows minimum, dependency matrix, or installation/launch/uninstall acceptance is attached to this candidate | Do not publish instructions as verified |
| Current screenshots | No current product screenshots available or approved | Publish official branding only; keep screenshot gallery empty with a precise capture checklist |
| Public version and release | No public version, tag, or GitHub Release | Leave Downloads unavailable |

The source fix for rectangular selection is present in the exact worktree fingerprint recorded for the 0.2.25 candidate. This establishes build provenance, but the executable was not launched for this review and the physical interaction has not been accepted.

## Why the earlier publication stopped

The available evidence is the previous task's conversation record and GitHub state. PR #1 had been prepared on a documentation branch but remained open; the prior plan required explicit approval before merging or creating a release. No release-creation or binary-upload attempt is recorded, and authentication failure was not the cause of the prior pause.

This recovery request authorizes safe public documentation. The current candidate still fails the binary gates, so no release was attempted. The CLI reports no authenticated GitHub host, and the connected GitHub tool supports repository content writes but not release creation or binary uploads. Those tool limits are secondary to the candidate's technical and distribution blockers.

## Required gates before a public pre-release

1. Approve an exact source cut and reserve a public version and channel.
2. Rebuild or repackage from that cut so the setup executable, runtime files, manifest, and integrity record are linked.
3. Decide the Authenticode signing policy and confirm distribution terms.
4. Verify install, launch, update/manual replacement, uninstall, and recovery.
5. Perform physical desktop selection, Start, Dock, Spotlight, QuickLook, and Aurora checks on that exact candidate.
6. Publish confirmed Windows requirements, dependencies, known limitations, and SHA-256 values.
7. Capture real product screens from the accepted candidate and review them for personal information.

## Scope and privacy

This public preparation adds product documentation and the official VoyagerOS emblem. It does not add development source, build folders, internal logs, private local paths, user data, saves, or unapproved runtime binaries. The repository has no license file; no license or redistribution terms were added.
