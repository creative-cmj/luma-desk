# Luma Desk 2.5.0 — find your desktop flow

A new Workflow page brings five tiling layouts, live visual controls and keyboard navigation to Luma. This is an independent desktop widget app, not a port of the Hyprland compositor.

## What works

- **Five layouts:** Master, Dwindle, Grid, Columns and Monocle. Adjust gaps and master width, choose a monitor, and arrange visible unpinned Luma widgets. Widget layout changes support undo.
- **Windows app tiling:** Select ordinary app windows to arrange them. Restore reverses their placement, including maximized state and the previous normal restore rectangle. Minimized, utility, shell and cloaked windows are excluded. This is a user-triggered arrangement; background automatic management is not enabled.
- **Command palette:** Ctrl+K on Windows or Command+K on Mac searches pages, Luma workspaces, widget visibility and recovery commands.
- **Widget scratchpad:** Tuck a widget away and bring it back without losing its content.
- **Live appearance:** Gradient borders, accent glow, translucent surfaces, and quiet/smooth/spring widget entrance animation. System and app reduced-motion preferences take priority. These are effects on Luma widgets, not OS-wide window decorations.
- **Workspaces:** Existing Luma presets switch widget arrangements while preserving current writing. OS virtual desktops remain separate.
- **Live config reload:** Validated `desktop-control.json` settings reload without restarting. Invalid configuration keeps the current settings active. This file contains data only; it cannot execute commands or scripts.

Existing sixteen widgets, nine themes, eighteen wallpapers and local format-4 notes/layouts are preserved. Desktop extension settings live in a separate file, so older versions can still read the core content format.

## Downloads

**Windows x64:** Setup.exe installs per user; Portable.exe runs without installation. Both save to the normal Luma Desk user profile. Quit the existing app before opening the updated one. Installer and portable builds are unsigned.

**Mac (macOS 13+):** Choose arm64 for Apple Silicon or x64 for Intel. Open the DMG and drag Luma Desk into Applications; ZIP bundles are alternatives. Mac builds are ad-hoc signed, without Apple Developer ID or notarization. macOS may block opening them; keep system security protections enabled.

Mac supports Luma widget layouts, visual settings, workspace/palette controls and scratchpads. **Other-app window tiling is Windows-only.** Mac widgets are transparent interactive windows and may rise when clicked. Wallpaper application uses macOS System Settings. Show Desktop/full-screen Spaces can hide widgets.

## Verification and practical limits

The release includes native Mac runner reports for both processors. Windows native tests use separate-process test windows, not the user's open apps, and verify exact position and maximize/normal-restore recovery. Widget renderers are denied app enumeration and window-control IPC. Existing theme, content-preservation, editor, restart, and packaged-app checks are also run.

Physical Mac interaction, Mac login/notification/Spaces behavior, quarantined-download installation, mixed-DPI Windows displays, actual display unplugging and real sleep/resume have not been manually verified.

The Explorer desktop-parenting limitation on the tested Windows build remains: ordinary transparent widget windows are used as a fallback; Show Desktop may hide them. Separate widget windows consume memory. Luma is not an OS shell or compositor replacement.

## Hyprland reference

Reference: https://github.com/hyprwm/Hyprland — BSD-3-Clause, copyright 2022–2026 vaxerski. Luma's new layout planner, Windows bridge and website styling are independently implemented. No Hyprland binary, logo, website media or C++ plugins are bundled. The full upstream source has been checked out separately in the local workspace at commit `8010b4e5c66f97aa82cd5b3332b4ec613779b9a7` with its original license.

Hyprland's Wayland rendering, Linux input protocols, tearing, C++ plugin manager, system-wide blur and native Linux workspace/group semantics are not implemented in Luma. Use Hyprland on a supported system for those capabilities. This project is independent and is not endorsed by Hyprland.
