# Windows 2.8 verification

Production TypeScript/Vite build and 48 unit tests pass, including duplicate checks, download state, explicit restart, persistence failure, offline retry and unsupported builds.

Packaged app updater test uses an isolated profile and local HTTP fixture hosting the exact release installer/metadata. The real electron-updater rejects a corrupted SHA-512, downloads the real NSIS artifact and yields a byte-identical executable. Settings displays readiness; clicking Restart saves a checkpoint and generates the actual NSIS --updated/--force-run command. Installer spawn and process quit are intercepted. Widget renderers and invalid commands are denied by the main process.

The running installed copy and personal profile are not replaced. Full installer replacement and a later live-version upgrade remain unverified. Windows builds are unsigned; checksum validation is not an Authenticode publisher signature. Only installed Windows Setup copies support updates. Portable, development builds and Mac preview do not. Existing physical mixed-DPI/Explorer/fullscreen compatibility limits remain.

For future releases: increment package version, build Windows NSIS with the GitHub publish configuration, run tests, then upload Setup.exe, its .blockmap, and latest.yml to the same stable release. Publish only once all assets are uploaded and verified; keep prior release assets for differential downloads. Never embed repository credentials in the app. Do not publish an unrelated latest stable release without Windows update metadata; keep Mac-only previews as prereleases or provide the matching Windows manifest.
