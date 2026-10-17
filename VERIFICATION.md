# Luma Desk 2.5.0 verification

## Passed

- TypeScript checks and production frontend/main builds.
- 38 unit tests, including tiling geometry, non-overlap, negative monitor positions, infeasible layout rejection, configuration validation and backup recovery.
- Native Windows Workflow UI and packaged executable: widget tiling/undo, scratchpad visibility, command palette, configuration reload and full restart persistence.
- Three separate-process test windows: native Windows tiling and exact restoration, including maximize state and normal restore geometry. Tests selected only task-owned fixture windows.
- Widget renderers cannot enumerate or arrange external application windows. Protected bridge calls are restricted to the customization renderer and payloads are validated.
- Existing Windows editor, drag/resize, group movement, keyboard control, theme/content preservation, safe import, monitor placement and restart regression.
- All sixteen widget library cards and native companion controls; all nine themes and migration checkpoint tests.
- Packaged Windows startup, local note persistence, close-to-tray, registered shortcut and sandbox/CSP checks. Portable wrapper startup also passes.
- Both Mac architectures built and launched on native standard GitHub-hosted runners: widget tiling, configuration, scratchpad, command palette, nine themes, local restart persistence, Windows-binding isolation and correct external-app tiling unavailability. Bundle signature integrity checked with codesign.
- Website: responsive layout, interactive five-layout preview, keyboard controls, nine-theme previews, video playback, links and FAQ at 1440, 768, 390 and 320 px.

Mac build/test run: https://github.com/creative-cmj/luma-desk/actions/runs/39056474670

## Conditions and limits

Windows 11 build 26200, x64, two 1920×1080 monitors at 100% scaling. Other Windows versions, mixed-DPI displays, physical display unplugging, actual sleep/resume and Explorer restart have not been manually verified. App minimum sizes may prevent an exact requested arrangement.

The tested Explorer shell rejects desktop parenting; widget windows use a fallback. Show Desktop can hide them. Mac uses interactive transparent windows, without Finder desktop attachment; full-screen Spaces can hide widgets. Physical Mac interaction, login, notifications and quarantined-download installation have not been manually tested. Mac requires 13.0 or later.

Windows executables are unsigned. Mac packages are ad-hoc signed; they have no Apple-trusted Developer ID or notarization. A successful codesign integrity check does not identify a trusted publisher. macOS may block these preview downloads.

Hyprland compositor/plugin/system-wide rendering features are not ported into this app. Read RELEASE-NOTES.md for the implemented features and platform distinctions.
