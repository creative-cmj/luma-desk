# Luma Desk 2.3.0 verification

Release target: Windows x64, installer and portable. Tested October 17, 2026 on Windows 11 build 26200 with two 1920×1080 displays at 100% scaling.

- 34 unit tests passed: atomic saves and corrupt-file recovery, old-format migrations and byte-identical backups, content persistence, reminder deduplication/deletion, safe import boundaries, arithmetic parser, layout history, display recovery and oversized-save protection.
- Actual editor tests passed: pointer drag/resize, cancellation, geometry validation, grouping, equal gaps, undo/redo, duplication and movement to the second real monitor.
- Desktop regression passed: seven original widgets, theme/preset preservation, timers, safe launch boundary, file icons, import validation, global shortcut conflict, full restart and close-to-tray.
- Packaged collection test passed: all sixteen library cards, native widget rendering, calculator, habits, countdown, planner, journal, stopwatch, breathing, thoughts and choices. Content and a running stopwatch survived a full restart.
- Packaged launch smoke passed: version 2.3.0, local save, sandboxed renderers, no Node access, network-disabled content security policy, registered test shortcut, panel renderer released on close while two widgets continued.
- Portable wrapper launched the offline app with two widgets.
- Authenticode checks: installer and portable are NotSigned. No signing identity is claimed.

The normal user's installed app and profile were left untouched. A fresh interactive install/uninstall of 2.3.0 was not performed because it could replace existing per-user installation registration. Installer packaging completed; installed payload and portable launch were tested separately. Earlier local installation testing is not substituted for this release's unverified install/uninstall path.

On this Windows build Explorer parenting returned Win32 error 87. Widgets used transparent fallback windows below ordinary applications, without always-on-top. Show Desktop recovery, physical display unplug/replug, mixed-DPI interaction, real sleep/resume and Explorer restart remain unverified. Pure geometry tests cover negative display coordinates, portrait arrangements and changing work areas; they do not establish physical-device compatibility.

A five-second two-widget idle sample, with the panel renderer closed and clock seconds off, totaled approximately 0.0635% reported CPU and 495 MiB summed working sets. Working sets include shared pages and are not unique memory; this is a brief observation, not a performance guarantee. No low-memory claim is made.

Public screenshots come from the packaged app using synthetic notes, tasks and habits. The runtime needs no account, cloud storage or API keys. Website browsing and GitHub downloads have their own service policies.

## 2.3 theme verification

Actual UI checks select all nine theme cards, verify live native widget accent/surface colors and both bundled wallpapers, reset customization, migrate version-three settings with byte-identical backup, and restart with Lavender selected and notes preserved.
