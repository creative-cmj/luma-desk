# Verification — Portl Beta 3.4.11

- TypeScript/Vite build and all 59 unit tests passed. Identity regressions cover the original profile location and both adjacent uninstaller names.
- Actual source launch with an isolated legacy appData directory verified the default original profile path, exact writing/Space names and appearance after restart.
- Broad source review passed all sixteen native widgets and enlarged pages; native desktop controls and shared writing passed.
- Packaged brand/profile/restart checks passed in light/dark and compact enlarged views.
- Actual executable and installer portal icon resources match the source ICO pixels at 16, 32, 48 and 256px. Shell icon-cache refresh was not tested.
- Packaged updater checks passed: corrupt SHA512 rejection, actual installer download/integrity, GUI ready/error states and save-checkpoint/install-command routing. Installer spawn and quit were intercepted.
- Setup SHA512 matches latest.yml; SHA256SUMS.txt covers the named release files.

Full installed-version replacement, physical mixed-DPI compatibility and a new Mac/Linux runtime release were not tested. Renderer zoom, native fixtures and direct embedded-icon extraction have those practical limits. Tests use isolated profiles; the personal installed app and data were not modified.

Only allowlisted binaries, update metadata, checksums and public documentation are released. Application source, private backups, credentials, launch helpers and test/personal profiles stay local.
