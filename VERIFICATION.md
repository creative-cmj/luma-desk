# Verification — Portl Beta 3.5.0

- TypeScript/Vite build and all **66 unit tests passed**. Coverage includes identity, monitor geometry, migration backup/write failures, exact writing, shared Spaces, launcher column validation, real system sampling and updater safeguards.
- Actual Electron source review exercised all seventeen native widgets and existing editing controls, light/dark collections, enlarged layouts, search/commands, keyboard/focus, exact save/restart and native desktop controls.
- **252 solid widget-text contrast measurements** across the reviewed palettes had no reported concerns. Additional app-control palette checks passed. These measurements do not establish contrast over every arbitrary wallpaper/gradient.
- Packaged premium review passed at 1672×941, 1366×768 and 1000×740 window sizes, including 150% renderer zoom. Canvas aspect ratio, pointer drag/resize with one-step Undo, real inspector theme/Space actions, new-widget selection, native launcher columns and exact restart were verified with no renderer errors.
- Packaged legacy format-five profile migration produced a byte-identical original backup and preserved exact writing, Space names and appearance after restart. Source tests additionally exercised the default original profile location.
- Packaged write-failure test preserved the previous file and editable writing, showed visible failure at compact/enlarged sizes, then persisted the successful retry and restored it exactly after restart.
- System values came from actual native OS readings. The integration test confirmed that ordinary Clock widgets received zero telemetry events; runtime samples did not persist. A bounded telemetry snapshot was substantially smaller than the full settings view in the isolated fixture. This is not a performance benchmark.
- Packaged updater rejected corrupt SHA512, downloaded and verified the actual installer, showed ready/error states and routed Restart/Quit through the real checkpoint/install-command path. Installer process launch and quit were intercepted: no personal installation was replaced.
- Executable and installer portal icon resources matched the source ICO pixels at 16/32/48/256px. Runtime preview/apply ribbon assets matched byte-for-byte at 1920×1080; original source artwork, source code, helpers and profiles were excluded from the application archive.
- Installer SHA512 matches latest.yml. SHA256SUMS.txt covers the listed release files; uploaded assets are checked against local digests before publication.

## Practical limits

Full installed-version replacement, physical mixed-DPI hardware, OS wallpaper application, shell icon-cache refresh, a new Mac/Linux runtime and arbitrary third-party launch targets were not tested in this release. Renderer zoom, controlled native fixtures and install-command interception have those practical limits. Windows desktop fallback is displayed honestly. Tests use isolated profiles; the personal installed app and data were not modified.

Only allowlisted binaries, update metadata, checksums, a sanitized screenshot and public documentation are released. Application source, private source backups, credentials, launch helpers and test/personal profiles stay local.
