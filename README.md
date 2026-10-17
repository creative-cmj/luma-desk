# Luma Desk

Local desktop widgets and personal Spaces. No app account, subscription, analytics or cloud sync.

[Windows 2.8 download](https://github.com/creative-cmj/luma-desk/releases/tag/v2.8.0) · [Website](https://luma-desktop-widgets.gentlechar18.chatgpt.site/) · [Mac 2.6 preview](https://github.com/creative-cmj/luma-desk/releases/tag/v2.6.0)

## Windows 2.8

Native desktop editing with snapping and alignment guides, multi-selection, keyboard controls, Undo/Redo, named Spaces with shared content, per-widget styling, searchable command palette, expandable widgets, optional desktop toolbar, temporary Peek and Focus Mode.

Quit the running copy, then install Setup.exe or run Portable.exe. Both use `%APPDATA%\Luma Desk`. The installer is per-user; builds are unsigned. Keep security protections enabled and review the release/checksum files.

The first run backs up format-4 settings before migrating to format 5. Older formats also receive original backups. To back up personal content, close Luma and copy the complete data folder. Restore the original backup before downgrading. Do not post profiles publicly: they can contain personal writing and paths.

Default desktop shortcuts: Control+Alt+E for editing, Control+Alt+K for command search, Control+Alt+P for seven-second Peek and Control+Alt+F for Focus Mode. Change or disable them in Settings. Control+K opens command search inside the panel.

Spaces are Luma widget workspaces, separate from OS virtual desktops. Ordinary application windows remain above widgets except during explicit Peek. Show Desktop and fullscreen applications can hide widgets on fallback Windows integration.

## In-app updates

Install Windows Setup 2.8 once. Luma checks GitHub at startup and every six hours, downloads stable updates in the background, then waits for Settings → Restart to update. It does not install on ordinary quit. A settings checkpoint is saved before starting the installer. No GitHub account is required. Your widget content is not uploaded. Offline errors leave the current version usable. Portable builds and the Mac preview still require manual updates.

## Other platforms

The separate Mac 2.6 preview remains available for Apple Silicon and Intel, macOS 13+. It is ad-hoc signed without Developer ID or notarization, and macOS may block it. The 2.7 Windows features are not claimed for Mac. No native Linux package is available.

[Full release details](RELEASE-NOTES.md) · [Verification and limits](VERIFICATION.md) · [Report an issue](https://github.com/creative-cmj/luma-desk/issues/new?template=bug_report.yml)

This public repository contains release binaries, documentation and verification workflows. Application source remains local. Independent project; it does not run the Hyprland compositor or its plugins.
