# VoyagerOS product roadmap

This roadmap has no promised dates. Work advances when the evidence for its exit condition is available.

## Now — create a releasable source and package

- Produce an owner-approved, exact source cut for public distribution.
- Reserve a public version and channel; do not reuse the private-alpha label.
- Tie the installer, executable, runtime modules, manifest, and hashes into one integrity record.
- Confirm distribution terms and decide how the unsigned state will be handled.
- Verify install, first launch, update, uninstall, and recovery instructions on a supported Windows configuration.

**Exit condition:** one candidate has matching source, identity, installer, integrity, requirements, and release notes, with distribution terms confirmed.

## Next — accept the desktop experience

- Exercise rectangular selection with a physical mouse on the exact candidate.
- Verify Dock appearance, Start gestures, search surfaces, hit testing, focus, and window ordering.
- Check display and DPI changes, multiple monitors, and return to the native Windows desktop.
- Capture current product views from the accepted candidate and review them for personal information.

**Exit condition:** physical and visual acceptance covers the candidate and any remaining limitations are documented.

## In parallel — validate Aurora and QuickLook

- Test Aurora with a real microphone and the Windows speech components that the candidate requires.
- Check privacy permission states and representative editable and non-editable target applications.
- Verify QuickLook presentation, supported file types, focus, close behavior, and shell shutdown.

**Exit condition:** repeatable acceptance evidence and explicit compatibility requirements.

## Later — use tester feedback

- Open the tester channel only after a verified public build exists.
- Use the privacy-aware [bug report](../.github/ISSUE_TEMPLATE/bug_report.yml) and [feature request](../.github/ISSUE_TEMPLATE/feature_request.yml) templates.
- Prioritize reproducible issues by user impact, release risk, and evidence.
- Update the roadmap after each release review.

No user-research findings, adoption numbers, or commercial outcomes are claimed before they exist.
