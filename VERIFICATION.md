# Verification — Luma Beta build 3.4.10

- Fresh TypeScript/Vite build and all 57 unit tests passed.
- Packaged Windows calendar/journal checks passed: compact 300/320px light/dark views, long event titles, separate delete controls, localized metadata, exact event deletion, journal labels and full restart preservation.
- Packaged native session/style checks passed: timer actions, calendar month/event creation, light/dark/custom palette parity, note recovery and exact writing.
- Packaged updater checks passed: corrupt SHA512 rejection, actual installer download and integrity validation, ready/error GUI states and save-checkpoint/install-command routing. Installer spawn and quit were intercepted; full installed-version replacement was not performed.
- Setup SHA512 matches latest.yml. SHA256SUMS.txt covers all release assets listed in it.

Renderer zoom and controlled native fixtures are not physical mixed-DPI, sleep/resume, fullscreen or Explorer compatibility proof. Windows x64 was tested; no new Mac/Linux runtime verification is claimed. Arbitrary wallpapers and translucent custom surfaces may affect perceived contrast.

The public repository contains binaries and documentation only. Source backups, personal profiles, writing, paths and test profiles are not published.
