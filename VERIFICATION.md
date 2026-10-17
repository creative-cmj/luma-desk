# Luma 3.0 Windows verification

- Production TypeScript/Vite builds and 49 unit tests pass.
- Packaged visual tests cover all six app pages, dark/light appearance, primary-action contrast ≥4.5:1, no horizontal page overflow at 1000/1600px, real layer selection/show/hide, and Space/appearance/content persistence after a complete restart. Widget colors stay independent of interface appearance.
- Editor regression covers expanded canvas/inspector, geometry validation and Apply/Revert, equal gaps, group selection, duplicate/undo, and actual second-monitor transfer.
- Native experience regression covers actual OS window bounds, keyboard and controlled-pointer gestures, guide security, shared Space content, widget expansion, per-widget appearance, Focus/Peek, shortcut conflicts and native toolbar behavior.
- Workflow regression tiles/restores three task-owned native windows and verifies renderer isolation and validated config reload.
- Packaged updater test uses the exact NSIS installer and real electron-updater, checking SHA512 rejection, download byte equality, settings UI, IPC restrictions, persistence checkpoint and manual restart. A second real updater quit handler generates the silent NSIS /S command without force-reopening Luma. Process spawning and quitting are intercepted in these fixtures.

The normal installed app/profile are not replaced by tests. Full installer replacement remains unverified. Windows binaries are unsigned; metadata checksums do not provide an Authenticode publisher signature. Physical mixed-DPI changes, Explorer restart, sleep/resume and all Show Desktop/fullscreen combinations remain compatibility limits. Mac 3.0 and Linux are not packaged or tested; Mac 2.6 preview remains separate.

## Release procedure

Increase the package version, build/test Windows NSIS with the existing GitHub provider, then upload Setup.exe, its .blockmap, latest.yml and checksums to one stable release before publishing. Preserve prior release assets for differential downloads. Never embed credentials in the app or publish user profiles. Mac-only preview releases must not displace the stable Windows update manifest. Public repository contains binaries/docs only; application source stays local.
