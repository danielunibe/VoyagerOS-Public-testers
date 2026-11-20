# VoyagerOS product decisions

These decisions describe the product and release boundaries visible in the current development and distribution plan. They do not imply that every feature has passed public acceptance.

## 1. VoyagerOS complements Windows

**Decision:** Build VoyagerOS as a native layer that coexists with the existing Windows desktop.

**Reason:** The product explores desktop interactions while preserving familiar Windows surfaces and application behavior.

**Trade-off:** Window ordering, focus, input, display changes, and multi-monitor behavior need explicit Windows acceptance before release.

## 2. Keep the native Windows runtime

**Decision:** The intended runtime uses Win32, Direct3D 12, DirectComposition, and a Rust core.

**Reason:** The product is designed around Windows desktop composition and native integration.

**Trade-off:** Claims about behavior depend on validation in the real Windows desktop, not only on code-level or synthetic checks.

## 3. Preserve the established VoyagerOS visual identity

**Decision:** Retain the Windows avatar, original artwork, and dark Dock material in the product presentation.

**Reason:** These assets and materials are part of the established project identity.

**Trade-off:** Public screenshots must come from the actual product and must be reviewed for personal information before use.

## 4. Separate development source from public distribution

**Decision:** Keep source development in its private repository. Use this public repository for approved downloads, documentation, and tester feedback.

**Reason:** Testers need a clear distribution surface without exposing internal files, audit logs, user data, saves, or build directories.

**Trade-off:** Each public package needs a verifiable connection to an exact source cut even though the source remains private.

## 5. Assign public versions from verified packages

**Decision:** Do not promise a public version number until a matching `PUBLIC` package exists and passes release checks.

**Reason:** The public number, EXE, installer, manifest, hash, and notes must refer to one artifact.

**Trade-off:** A planned number can change before the first release; private-alpha labels do not become public versions.

## 6. Keep update instructions honest

**Decision:** Describe GitHub Releases as the manual update channel until an in-app updater is implemented and verified.

**Reason:** Users should not expect automatic downloads or installation behavior that the product does not provide.

**Trade-off:** Testers will need to check Releases and install each approved update themselves.
