# Verification — Portl Beta 3.6.0

- TypeScript/Vite build and all **70 unit tests passed**, including starter geometry/content preservation, invalid requests, exact restart and measured neighboring gaps. Existing migration, atomic-save, contrast, layout, telemetry and updater regressions pass.
- Actual source review passed all **17 native widget types**, six app pages at 1000/1600px and 100/125/150% renderer zoom, existing dialogs/keyboard/menu controls, shared content and full restart.
- Packaged guided-studio test passed setup style/widget/display preview, new Space creation, old layout and exact writing preservation, side-effect-free starter cancel, useful quick controls reflected in actual native text/font/opacity, coordinated theme preview/style controls, actual drag guides and Escape geometry restoration, keyboard focus containment, compact/enlarged layouts and full restart.
- Packaged premium-editor regression passed aspect-preserving preview sizing, real theme/Space inspector actions, pointer drag/resize and Undo, native launcher columns, new-widget selection, telemetry and exact restart.
- Packaged save-failure/retry test preserved the previous settings file and exact writing and restored the successful retry after restart. Packaged legacy profile migration preserved a byte-identical format-five original backup and exact writing.
- Packaged updater rejected a corrupt SHA512, downloaded and verified the actual installer, displayed ready/error states and routed Restart/Quit through save-checkpoint and real install commands. Installer spawn/quit were intercepted.
- Native executable and installer portal icon resources match source ICO pixels at 16/32/48/256px. Packaged version/app ID and runtime wallpaper parity were checked; private source, test profiles and helpers were excluded from the app archive.
- Installer SHA512 matches latest.yml. Release asset uploads are checked against local sizes and SHA256 digests, and SHA256SUMS.txt covers the listed release files.

All GUI tests use isolated profiles; the user's installed copy and personal data were not modified. Renderer zoom does not prove physical mixed-DPI behavior. Full installed-version replacement, OS wallpaper apply, shell icon-cache refresh and a new Mac/Linux runtime were not tested. Windows binaries remain unsigned. Starter images are explicitly layout previews, not invented live readings. No FPS or broad performance benchmark claim is made.

Only allowlisted binaries, update metadata, checksums, sanitized public documentation and the reviewed screenshot are uploaded. Application source, private backups, test/personal profiles, credentials and launch helpers stay local.
