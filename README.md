# Luma Desk

Your desktop, in full flow. Sixteen local widgets, nine themes, five tiling layouts, keyboard commands and personal widget workspaces.

[Download Luma Desk 2.6.0](https://github.com/creative-cmj/luma-desk/releases/tag/v2.6.0) · [Website](https://luma-desktop-widgets.gentlechar18.chatgpt.site/) · [Report a problem](https://github.com/creative-cmj/luma-desk/issues/new?template=bug_report.yml)

Windows x64 installer and portable builds; Mac preview for Apple Silicon and Intel (macOS 13+). Windows builds are unsigned. Mac builds are ad-hoc signed, not Developer ID signed or notarized, and may be blocked by macOS.

## A clearer space

Version 2.6 adds coordinated light and dark control-panel interfaces, original vector icons, a sidebar workspace picker, and a desktop overview. Widget and theme galleries have clearer previews and controls. Choose the sun/moon button to change the interface; your widget colors stay independent. Both choices survive a restart.

## Workflow

Choose **Workflow** in the app. Pick Master, Dwindle, Grid, Columns or Monocle, adjust gaps and main-window share, select a monitor, and arrange Luma widgets. Unlock the layout first. Undo restores the previous widget layout.

On Windows, refresh the app-window list, select only the windows you want to move and choose Arrange. Restore brings back their previous placements. Other-app tiling is not available on Mac. This is manual arrangement, not an automatically running window manager.

Use **Ctrl+K / Command+K** for command search. Switch Luma workspaces, tuck widgets away and bring them back, or recover a missing layout. Luma presets are separate from OS virtual desktops.

Gradient borders, adjustable glow, translucent surfaces and widget entrance motion update live. Reduced-motion preferences are respected. These settings affect Luma, not every OS window.

## Install and keep your content

Windows: run Setup.exe, or launch Portable.exe without installation. Quit the existing version before starting the new one. Both share `%APPDATA%\Luma Desk`.

Mac: open the DMG, drag Luma Desk into Applications, and launch it there. For a ZIP, extract and move the app bundle into Applications. Select arm64 for M-series Macs and x64 for Intel. Data saves in `~/Library/Application Support/Luma Desk`. Wallpapers are set in macOS System Settings. Widgets can rise when clicked and may be hidden by Show Desktop or full-screen Spaces.

Close Luma before backing up its data folder. Existing format-4 content remains compatible. New workflow settings use a separate `desktop-control.json`; existing notes and presets are not converted to a new format. Do not share profiles publicly: they may contain private writing and file paths.

## What Luma is

An independent Electron desktop widget app inspired by customizable, keyboard-led workflows. It does not run the Hyprland compositor or Linux C++ plugins. [Full capabilities and limitations](RELEASE-NOTES.md). [Verification notes](VERIFICATION.md).

This public repository hosts release binaries, documentation and build-verification recipes. Application source remains local. No app account, cloud sync, API key or subscription is required.
