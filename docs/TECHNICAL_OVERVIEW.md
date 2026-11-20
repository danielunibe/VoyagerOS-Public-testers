# Technical overview

This is a high-level description of the active development architecture. It omits private source, machine paths, internal logs, and implementation secrets.

## Runtime

The active desktop shell is a Windows-only C++20 application built with CMake. It uses Win32 windows and message procedures for desktop integration, Direct3D 12 for native rendering, and DirectComposition for composed surfaces.

Rust core and Windows-platform components are built as runtime modules and connected to the native host through a defined ABI. The C++ bridge checks ABI data before consuming core state. This keeps platform-specific windowing and rendering in the native shell while providing a separate Rust component boundary.

## Interaction path

~~~mermaid
flowchart LR
    U[Pointer and keyboard input] --> H[Win32 native host]
    H --> R[Window procedure and input routing]
    R --> S[Surface and feature policies]
    S --> D[Desktop and selection]
    S --> K[Dock and Start]
    S --> Q[Spotlight and QuickLook]
    S --> P[Settings and personalization]
    S <--> C[Rust core and Windows platform modules]
    S <--> W[Windows shell, speech, and audio services]
    D --> G[Direct3D 12 and DirectComposition]
    K --> G
    Q --> G
    P --> G
~~~

The diagram describes component boundaries, not a claim that every surface has passed visual or physical QA.

## Main responsibilities

### Native shell

- Creates and manages host windows, focus, activation, and window-procedure dispatch.
- Routes pointer and keyboard events to the surface that owns the interaction.
- Keeps the desktop selection surface separate from Dock and overlay interaction policies.
- Coordinates shell startup and shutdown with feature lifecycles.

### Rendering and composition

- Uses Direct3D 12 and Windows graphics APIs for native rendering.
- Uses DirectComposition to present composed desktop surfaces.
- Keeps the established dark Dock material and the original project assets.

### Feature surfaces and state

- **Desktop:** selection, desktop item interaction, and contextual actions.
- **Dock and Start:** pointer magnification and tap, double-tap, and hold gesture policies.
- **Spotlight:** search query and direct-answer evaluation.
- **Aurora:** contextual push-to-talk, Windows speech integration, and audio metering.
- **QuickLook:** native preview creation, closure, and teardown.
- **Settings:** native Win32 settings controls and persistence.
- **InputRouter:** registration of interactive overlay regions.

These are development components. Their release readiness is described separately in the [feature matrix](FEATURE_MATRIX.md).

## Windows integration

VoyagerOS integrates with the Windows windowing and shell environment. Aurora also depends on system speech and audio facilities, microphone availability, permission state, and the active target application. Those device and application conditions require real Windows acceptance.

## Validation model

Automated CTest records and focused component tests verify selected code paths and contracts. A successful component test does not establish that the complete application installs, launches, behaves correctly on multiple displays, works with a real microphone, or meets visual acceptance.

The local 0.2.25 build record contains a 230/230 automatic CTest result, and the focused desktop-selection regression test passed a fresh 1/1 run in this review. These results belong to development evidence; the candidate remains PRIVATE_ALPHA and has not completed physical release-candidate QA.
