# Luma Desk 3.0.0 — Desktop Studio

## A new layout and visual system

- Full-width top navigation with a persistent Space switcher and save status.
- Larger desktop canvas, a consolidated editing toolbar, and a widget layer list. Select widgets and hide/show them directly from the list; Shift-click selects groups.
- Dedicated scrolling properties inspector, including in expanded editing.
- Charcoal and lavender dark mode, warm light mode, refreshed cards and controls across Themes, Widgets, Workflow, Spaces and Settings.
- Existing notes, tasks, widget themes, shortcuts, Spaces and format-5 data are preserved. Changing the interface appearance does not change your widgets.

## Updates install when you quit

Windows Setup copies download stable updates in the background. Once a download is ready, choosing Quit Luma installs it silently. Luma saves a settings checkpoint first; a save failure postpones quitting and installation. Closing the panel keeps Luma in the tray. Restart to update is still available for immediate installation.

If you already have Setup 2.8: choose Settings → Check for updates → Restart to update once to get 3.0. From 3.0 onward, downloaded updates install on quit. No website re-download is needed for the 2.8 Setup upgrade. Portable and Mac preview copies still update manually.

Windows builds remain unsigned. Mac 2.6 preview remains unchanged. No Linux package is included.

## Tested

49 unit tests; packaged visual checks in light/dark mode at 1000/1600px; widget layer selection and visibility; Space/content persistence through restart; real editing, geometry, multi-selection, undo/redo, native movement, Workflow window tiling and restoration. Packaged updater tests validate real installer downloads, checksum rejection, manual restart and the silent install-on-quit command after a checkpoint. Installer spawning is intercepted to preserve the running installation: full installed-version replacement has not been exercised.
