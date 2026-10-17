# Luma Desk 2.4.0 — Mac preview

Luma's sixteen local widgets and nine themes, now packaged for macOS.

## Choose your download

- **Apple Silicon (M-series):** Luma-Desk-2.4.0-Mac-arm64.dmg
- **Intel:** Luma-Desk-2.4.0-Mac-x64.dmg
- ZIP versions of each app are available as alternatives.

Open the disk image and drag **Luma Desk** into **Applications**, then launch it there. For a ZIP, extract it and move Luma Desk.app into Applications. Apple menu → About This Mac identifies your chip or processor.

This is an early Mac preview. It is **ad-hoc signed, without an Apple Developer ID or Apple notarization**. macOS may block opening it. Keep system security protections enabled. A signed, notarized release requires an authorized Apple Developer identity, which has not been configured.

## Mac behavior

- Widgets are interactive transparent windows, without always-on-top behavior. Clicking them may raise them above another app. Finder desktop-layer attachment is not implemented.
- Close the settings panel to keep widgets running. Reopen using the menu bar icon or Dock; quit with Command+Q or the menu.
- The default show/hide shortcut is Control+Option+Space (Windows calls Option Alt). Change it in Settings if it conflicts.
- Wallpapers can be previewed in Luma; apply a desktop wallpaper using macOS System Settings. Automatic wallpaper application remains Windows-only.
- Open at Login is optional; enable it only after moving the app into Applications.
- Notes, layouts and other content save locally in `~/Library/Application Support/Luma Desk`. Quit Luma before copying this folder for backup. No account or cloud connection is needed by the app.
- Full-screen Spaces and Show Desktop may hide widgets. Menu bar, notification and login behavior can differ by macOS release.

## Verification

Both architectures are built on native standard GitHub-hosted Mac runners. Release assets include separate architecture-specific verification reports. These cover packaged app startup, live widget renderers, theme changes, native positioning, non-topmost windows, and persistence across restart. Signature integrity is checked using codesign. This is not a verification of an Apple-trusted publisher.

Physical Mac interaction, accessibility behavior, login, notifications, Spaces, sleep/resume, and installation of a quarantined download have not been manually tested. Refer to the reports for the exact tests that passed.

Windows stable downloads remain version 2.3.0. This Mac preview does not change your Windows installation.
