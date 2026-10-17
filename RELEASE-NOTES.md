# Luma Desk 2.8.0 — Windows in-app updates

Install this Windows Setup release once to enable future automatic downloads. Existing 2.7 and earlier copies do not have an updater and need this one manual installation.

- Settings shows installed version, update status, download progress and Restart to update.
- Installed Windows copies check after 15 seconds and every six hours. Stable releases only; no automatic downgrade.
- Updates download from the public GitHub release feed and are checked against release SHA-512 metadata. No account or widget-content upload.
- Updates install only after explicit Restart to update. Notes and layouts are flushed with a timestamped settings checkpoint first. Ordinary quitting does not install an update.
- Portable builds and the Mac 2.6 preview require manual updates. Mac signing and packaging work is still needed for automatic updates there.

All 2.7 desktop features and format-5 data remain. Windows packages are unsigned. Quit an older running Luma before installing Setup.

## Verification

48 unit tests and packaged updater checks. A real NSIS installer was downloaded through electron-updater and matched byte-for-byte. A corrupted SHA-512 was rejected. Settings UI, renderer permissions, backup and actual installer arguments were verified. Installer spawning/quit were intercepted to protect the existing installation: a complete installed-version replacement has not been exercised on this host.
