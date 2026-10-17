# Luma Desk

Sixteen useful Windows desktop widgets, arranged your way. Luma Desk runs locally without an account or subscription.

**Windows x64 · 2.3.0 · unsigned community release**

[Download the latest release](https://github.com/creative-cmj/luma-desk/releases/latest) · [Report a bug](https://github.com/creative-cmj/luma-desk/issues/new?template=bug_report.yml)

[Visit the Luma Desk website](https://luma-desktop-widgets.gentlechar18.chatgpt.site/) for real screenshots, theme previews and a short interface tour.

![Actual Luma Desk 2.3.0 theme gallery](https://luma-desktop-widgets.gentlechar18.chatgpt.site/assets/themes-2.3.png)

## New in 2.3

Six more palettes: Ocean, Forest, Sunset, Rose, Lavender and Midnight. Each has two matching offline wallpapers. Theme selection updates the live widgets and layout preview. Colors, opacity and typography remain customizable.

Settings/preset format is now **4**. Formats 1–3 upgrade with an untouched timestamped backup, keeping notes and layouts. Older app versions cannot read format 4; restore the original backup before downgrading.

## Your everyday, within reach

- Clock, sticky notes, tasks, app launcher, focus timer, calendar and quick links.
- Calculator, countdown, habits, weekly planner, journal, stopwatch, breathing, daily thought and decision tools.
- Neon, Cozy, Minimal, Ocean, Forest, Sunset, Rose, Lavender and Midnight themes; local wallpapers; editable widget colors, typography and transparency.
- Move, resize, align, lock and undo in a visual editor. Save different layouts as presets; up to twelve widgets per layout.
- Local saving, versioned migration backups and layout-only exports that omit personal content.

## Install

Download **Luma-Desk-2.3.0-Setup.exe** from Releases, run it, choose a per-user location, and launch Luma Desk. The alternative **Portable.exe** runs without installation but stores settings in your Windows user profile, not beside the executable. Both variants share the normal Luma Desk profile; quit one before opening the other.

These builds are unsigned. Windows may show an unknown-publisher warning; no code-signing identity has been verified. Review the release and checksums before deciding whether to run it. Do not disable Windows security or antivirus.

Choose **Widgets** to add a companion, enable **Edit Layout** to move or resize, and lock the layout when finished. Close the panel to keep widgets running. Reopen from the tray; **Ctrl+Alt+Space** shows or hides widgets. Quit from the tray or Settings to close the app.

## Compatibility and limitations

Tested on Windows 11 build 26200, x64, two 1920×1080 displays at 100% scaling. Other Windows versions, mixed-DPI setups, physical display unplugging, real sleep/resume and Explorer restart have not been verified for this release.

On the tested Windows build Explorer rejected desktop parenting. Luma uses a transparent-window fallback below ordinary application windows, without always-on-top behavior. **Show Desktop may hide widgets**; use the tray or shortcut to restore them. This is not a Windows shell replacement. Separate Electron widget windows can use substantial memory; no low-memory claim is made.

## Privacy and recovery

Luma's runtime needs no account, API key or cloud connection. Notes, tasks and layouts save locally in `%APPDATA%\Luma Desk`. Deliberately opened websites use your default browser. Back up this folder while Luma is closed; uninstall preserves it. Do not upload settings files publicly: they can contain personal writing and local file paths.

If widgets disappear, open Settings from the tray and choose **Recover Off-Screen Widgets**, then **Show widgets**. If a shortcut conflicts, change it in Settings. Moving a restored widget deliberately makes its new placement the intended position.

This repository distributes release binaries, documentation and issue tracking. It does not contain the application's source code. The application license and third-party notices ship with the release.

## Feedback

[Open an issue](https://github.com/creative-cmj/luma-desk/issues). Include the version, Windows build, display scaling and steps to reproduce. Use synthetic notes in screenshots; remove names, private text and file paths. Avoid posting full settings or diagnostic files publicly.
