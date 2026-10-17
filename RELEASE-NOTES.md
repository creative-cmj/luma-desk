# Luma Desk 2.6.0 — a clearer space

Luma's control panel has a new visual system: clearer navigation, calmer surfaces, original vector icons and coordinated light and dark interfaces.

## What changed

- Switch the control panel between light and dark using the sun/moon button. The preference saves locally and stays separate from widget themes.
- Switch your real widget workspace directly from the sidebar. Current notes follow their widgets without being rolled back.
- See visible widgets, the selected workspace and connected displays in the desktop overview.
- Browse nine palette cards with color swatches and sixteen widget cards with consistent vector icons.
- Use clearer editor controls, settings, dialogs and command search. Secondary quick actions sit below the editor to leave room for the canvas. Short windows receive a compact sidebar.
- Keyboard focus, reduced motion and undo/redo are retained. Fonts and icons work offline; no remote design dependency is added.

Existing widgets, themes, wallpapers, tiling, scratchpads and content remain available. Core data stays format 4; there is no new notes/layout migration. Interface appearance is a separate local panel preference.

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
