# Luma Desk 2.7.0 — your desktop, within reach

This Windows update adds working desktop editing, shared-content Spaces and quicker widget interactions to the native Electron app.

## Use it

- **Edit Desktop:** enter from the tray, desktop toolbar or control panel. Default global shortcut: Control+Alt+E. Use the top handles to drag and the corner to resize. Shift-click widgets or handles to build a selection. Alignment guides show snapped edges/centers and equal gaps. Hold Alt while dragging to bypass snapping.
- **Keyboard editing:** arrows move the selection; Shift moves farther; Control+arrows resize; Control+D duplicates; Control+A selects unlocked widgets. Undo/Redo use Control+Z / Control+Y. Escape cancels an active gesture or exits editing. Text fields retain their normal typing and arrow-key behavior.
- **Command search:** Control+K inside the panel, or configurable global Control+Alt+K. Add notes/clocks, start focus timing, show your launcher, switch Spaces or themes, lock the layout, show/hide or recover widgets. Recent commands stay locally on the computer.
- **Spaces:** existing saved presets now appear as Spaces. Gaming, School and Chill starters, previews, create/rename/duplicate/delete, and optional global shortcuts remain local. Share or move an existing widget into another Space from its style inspector. Sharing keeps one live content identity. Pin across all Spaces is distinct from locking a widget's position. Unpin before deleting a globally pinned widget.
- **Personal styling:** open a widget's inspector and expand “This widget’s style & Space”. Change its accent, surface, background opacity, font size, corners, border, shadow and density. Reset widget to theme removes its overrides; text opacity stays independent from surface opacity.
- **Responsive widgets:** clocks expand into a month view; launchers expand into a searchable list/grid; expanded focus timers show work/break lengths and the local finish time. Collapse restores the compact rectangle. Notes gain quick tint/font controls, and to-do widgets can hide completed tasks directly.
- **Desktop toolbar:** optional in Settings, and visible during editing. Quick-add, Space switching, editing, selection actions, history, Peek and Focus Mode. Optional auto-hide collapses it to a small handle 18 pixels inside the work area, away from the taskbar.
- **Peek:** explicitly raises the current Space's Luma widgets for seven seconds, then restores their previous visibility and non-topmost behavior. Default global shortcut: Control+Alt+P. This is a temporary overlay, not a permanent always-on-top desktop.
- **Focus Mode:** hides only Luma widgets marked “Hide this widget in Focus Mode”. Default global shortcut: Control+Alt+F. End Focus restores them. It does not manage other applications or Windows virtual desktops.

Shortcuts can be reassigned or disabled. Invalid or conflicting assignments retain the previous registrations. Native editing polls the cursor only during an active drag; hidden widget windows are destroyed after a brief departure transition. System and app reduced-motion settings take priority.

## Install and data

Quit your running Luma copy, then run the Windows x64 Setup.exe. The portable launcher is an alternative; it still uses the normal Windows profile. Both builds are unsigned. Keep Windows protections enabled and review the checksums before running.

The app upgrades settings format **4 to 5** to store new widget preferences. It first creates an untouched timestamped settings.v4-backup file. Existing notes, tasks, reminders, positions and saved layouts are retained. Formats 1–3 also migrate with an original backup. Back up the entire data folder with Luma closed. Restore the original backup before downgrading: older app versions cannot read format 5.

No app account, subscription, analytics, cloud sync, API key or remote font dependency is added. Settings writes remain validated, atomic and debounced; pending writes flush on exit.

## Platforms and limits

This release contains **Windows x64** packages. The separately available [Mac 2.6 preview](https://github.com/creative-cmj/luma-desk/releases/tag/v2.6.0) is unchanged and has not been upgraded or tested for 2.7 features. There is no native Linux package.

Windows 11 build 26200 was tested with two 1920×1080 displays at 100% scaling. Negative coordinates, portrait work areas, mixed scaling metadata and disconnect/reconnect recovery are covered by deterministic geometry tests. Physical mixed-DPI display changes, real sleep/resume, Explorer restart, Show Desktop and full-screen application behavior have not all been manually tested for this release.

The existing Windows desktop integration remains. On the tested Windows build Explorer rejects desktop parenting, so Luma uses ordinary transparent fallback windows below normal apps. Show Desktop or full-screen apps may hide widgets. Recover Layout and the tray show/hide action remain available. Peek is explicitly temporary; this is not an OS shell or Hyprland compositor replacement.

Separate Electron widget windows use substantial memory. The included idle sample is a short observation from an isolated fixture, not a lightweight/performance guarantee.
