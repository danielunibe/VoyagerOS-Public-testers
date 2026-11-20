# VoyagerOS product decisions

This record explains decisions visible in the implementation and the current release process. It does not claim user research or that every capability is release-ready.

## 1. Complement Windows rather than replace it

**Decision:** build VoyagerOS as a native desktop layer within the existing Windows session.

**Evidence:** the active runtime uses Win32 windows, window procedures, and Windows system integration.

**Trade-off:** focus, z-order, input routing, display changes, and multi-monitor behavior must be validated on a real Windows desktop.

## 2. Keep the native rendering path

**Decision:** retain the C++20 Win32 host with Direct3D 12 and DirectComposition, alongside the Rust core and Windows-platform components.

**Evidence:** the active CMake target links the Windows graphics and composition libraries; the native bridge loads Rust components through an explicit ABI.

**Trade-off:** code-level contracts are useful but do not prove visual quality, hardware compatibility, or runtime behavior on a tester's machine.

## 3. Preserve the established visual identity

**Decision:** retain the dark Dock material and original VoyagerOS brand artwork. Public visuals must come from the product or approved assets.

**Evidence:** this preparation publishes the official project emblem and deliberately excludes old beta imagery and QA fixtures as current product screenshots.

**Trade-off:** the gallery remains incomplete until authentic current captures can be made and privacy-reviewed.

## 4. Prioritize visible stability risks

**Decision:** treat the desktop rectangular-selection crash as a release blocker and prioritize its source repair and regression coverage.

**Evidence:** the older installed private-alpha build had a confirmed crash on that interaction; the development source contains the fix and the focused test passed.

**Trade-off:** source and automated results cannot substitute for exercising the exact installer and executable with a physical mouse.

## 5. Assign versions from verified packages

**Decision:** do not publish a version based only on a draft, source version, or executable file.

**Evidence:** the local 0.2.25 candidate identifies itself as PRIVATE_ALPHA and its installer is not linked to the build-identity artifact list.

**Trade-off:** the public version remains unassigned until the exact source cut, runtime, setup package, tests, and release notes agree.

## 6. Keep distribution and development source separate

**Decision:** use the public repository for approved documentation, release packages, and tester feedback; keep private development files, audit evidence, user data, saves, and build folders out of it.

**Trade-off:** each package needs a complete, reviewable provenance record even though the development source is not mirrored here.

## 7. Describe updates honestly

**Decision:** until a verified updater exists, describe the future update path as manual through GitHub Releases.

**Trade-off:** testers must download and install a published update themselves. No automatic update behavior is promised.

## 8. Do not invent licensing or validation

**Decision:** do not add a license, assert open-source status, or describe unrun QA as passed.

**Evidence:** the repository currently has no license file; the exact candidate has not completed physical or installation acceptance.

**Trade-off:** distribution remains blocked until the owner confirms terms and release gates pass.
