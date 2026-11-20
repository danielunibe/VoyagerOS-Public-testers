# Public release preflight — 2026-11-20

## Summary

**Documentation review: ready for review. Public download: blocked.**

The public repository is a distribution and tester-feedback channel, separate from the private development source. At the time of this review, its `main` branch has no version tags or GitHub Releases. The previous documentation named 0.2.1 as a planned initial version, but no artifact or release with that version exists.

## Artifact inventory

| Item inspected | Observed state | Public decision |
|---|---|---|
| Local development package 0.2.24 | Windows x64; package manifest labels it `PRIVATE_ALPHA`; package and EXE are unsigned | Exclude from public downloads |
| 0.2.24 build identity | Records a modified source tree and worktree modifications; records 224/224 automated CTest results | Not an exact public source cut; the test record is context for this private-alpha build only |
| Public package | No candidate with channel `PUBLIC` was available for this review | Do not assign a public version or write release notes for an artifact |
| Public screenshot | None included in this preparation | Add only after an actual product capture is available and reviewed for privacy |
| Public releases and tags | None found | Keep the Releases page empty |

The inspected private-alpha package is not a substitute for a public build. Its test record does not establish acceptance of a public artifact, and its unsigned state must not be represented as signed.

## Release blockers

1. Produce a `PUBLIC` package from an exact, attributable source cut.
2. Match the version, architecture, installer, EXE, manifest, and release notes.
3. Verify installation, launch, uninstall, and recovery behavior on a supported Windows configuration.
4. Finalize and publish requirements, dependency details, SHA-256 values, signature status, and known limitations.
5. Complete human visual and physical interaction acceptance for the exact candidate.
6. Decide whether the public unsigned-package limitation is acceptable or whether signing is required.

## Privacy and scope review

This preparation adds public-facing product and release documentation only. It does not copy source code, local file paths, internal audit logs, user data, saves, build outputs, or debug files into the public repository.

No public artifact, version tag, or GitHub Release is created by this preflight. The release remains unpublished pending candidate verification and the owner's publication decision.
