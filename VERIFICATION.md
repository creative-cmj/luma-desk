# Luma Beta build 3.1.0 — verification

## Actual app review

Baseline: ran packaged 3.0.1 with task-owned sample content; inspected desktop, library, Themes, Settings, Spaces and Workflow screenshots.

Cycle 1: removed redundant desktop context, promoted Save Space, collapsed secondary tools, created static theme-aware gallery previews and sectioned Settings. Ran and inspected the revised screens.

Cycle 2: consolidated shared materials/tokens; refined widget ink, materials and icon consistency; introduced one focus boundary for app dialogs and command search. Inspected first-run/rename and actual native widgets.

Cycle 3: enlarged-text testing exposed overlapping navigation; fixed with a responsive second row. Native review exposed single-line task editing; long tasks now wrap. Corrected Settings alignment and layer-list scrolling. Re-ran affected checks.

## Verified

- Production TypeScript/Vite build and 51 unit tests, including readable primary/secondary text against solid theme/custom surfaces and independent background alpha.
- Packaged refinement flow: Save Space; secondary controls; Settings keyboard tabs; dialog Escape/Tab/restore and draft preservation through IPC; onboarding; command empty state and close control; library search/full recovery.
- Six pages at app-window widths 1000 and 1600, with renderer zoom 100%, 125%, 150%: no horizontal page overflow.
- All sixteen real native windows captured in default and representative populated states; long task wrapping/focus; Neon, Cozy and Minimal notes; 65% background alpha with widget/text opacity 1.
- Exact state persists through a complete process restart. Separate native experience and functional collection regressions cover geometry, group editing, shared content, timers/tools, theme switching, toolbar/Peek/Focus and permission boundaries.
- Real electron-updater downloads the exact NSIS artifact, rejects a corrupted SHA512, preserves data checkpoints and generates manual/silent-on-quit installer commands. Spawn/quit are intercepted, so this does not prove full installer replacement.

Tests use isolated profiles. The normal installation and personal profile are untouched. The release includes safe report JSON and representative actual-app captures; profile files are never published.

## Limits

Physical mixed-DPI transitions, monitor unplugging, sleep/resume, Explorer restart and all Show Desktop/fullscreen combinations are not manually exercised. OS-native context menus and notifications remain native; renderer screenshots do not capture their appearance. Solid-surface contrast is measured; arbitrary wallpapers beneath translucent custom midtone surfaces can change perceived contrast. Windows binaries are unsigned. Mac 3.1/Linux packages are not built or tested; Mac 2.6 preview stays separate.

The three-second idle CPU/memory sample records real Electron processes with two visible widgets and the static-preview library. It is not a benchmark, long-run measurement or lightweight-memory guarantee. Multiple Electron windows still cost memory.

## Future updates

Keep build versions increasing, preserve the existing app ID/productName, publish the exact Setup.exe, blockmap and latest.yml together, then publish the release only after tests/hash checks. Keep prior release assets for differential downloads. Do not publish credentials, user profiles or local application source to the binary/documentation repository.
