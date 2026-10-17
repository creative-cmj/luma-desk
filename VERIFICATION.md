# Luma Desk 2.7.0 — Windows verification

## Verified

- TypeScript and production builds; 44 unit tests.
- Original settings format 4 migrates to 5 with a byte-identical timestamped backup. Atomic-save/corrupt-primary recovery and malformed/import rejection remain covered.
- Native executable: command palette creates a real note window; typing and arrow-key text editing retain its position. Quick tint and font controls update the note.
- Keyboard editing updates actual Windows widget bounds with snapping, resizing, group movement, Undo and Redo. The native alignment-guide window renders and is non-focusable/click-through; its renderer cannot execute desktop actions.
- Shared-content Space switching, pinning a clock across Spaces, live per-widget surface/opacity, clock/calendar expansion and exact compact-bound restoration.
- Focus Mode hides only marked Luma widgets. Seven-second Peek automatically restores non-topmost behavior; hidden-state Peek also restores its original visibility flags.
- Conflicting global shortcut assignments retain previous active bindings. Space shortcuts register. Optional native toolbar expands/collapses within the monitor work area and cannot enumerate external applications.
- A complete process restart preserves saved state and desktop-control preferences.
- Existing editor, personal content, sixteen widgets, nine themes, local reminders, file-launch safety, import, monitor placement and native selected-app tiling/restore regressions pass.
- Packaged startup, close-to-tray, local save, sandbox and portable-wrapper launch checks run against the 2.7 executable.

Tests use isolated profiles and task-owned fixture windows. The running installed copy and normal user data are not used or overwritten during testing.

## Measurement

The release includes an actual Electron idle-process sample: three visible widgets, the panel and optional toolbar, sampled over three seconds. CPU percentages and working/private memory are recorded by process. This is an observation on this Windows host, not a benchmark or performance guarantee. Multiple Electron renderer windows consume substantial memory.

## Limits

Host: Windows 11 build 26200 x64, two 1920×1080 monitors at 100% scaling. Negative/portrait work areas, mixed scaling metadata and disconnect/reconnect recovery are deterministic tests. Physical mixed-DPI changes, unplugging displays, real sleep/resume, Explorer restart and all full-screen/Show Desktop combinations were not manually exercised for this release.

The existing Explorer fallback limitation remains: Show Desktop can hide ordinary transparent widget windows. Widgets are below ordinary applications except during explicit temporary Peek. No Windows virtual-desktop manager or Hyprland compositor is bundled.

Windows executables are unsigned. Mac 2.7 and Linux builds are not provided or verified. Mac users can continue to use the separate 2.6 preview.
