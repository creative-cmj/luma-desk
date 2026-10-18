# Luma Beta — build 3.1.0

A calmer, clearer app, refined through repeated actual-app inspection rather than another wholesale redesign.

- A shared midnight/lavender and light design system with softer depth, consistent controls, readable labels and restrained motion.
- A higher desktop preview and a prominent Save Space action. Secondary selection/alignment controls reveal when needed; all editing features remain.
- A widget library with static theme-aware previews, readable cards, search counts, useful empty/full states and a route to another Space when full.
- Four keyboard-accessible Settings sections: Everyday, Desktop controls, Updates, Help & compatibility.
- Focus-managed rename, confirmation, import and first-run dialogs. Escape cancels, Tab stays inside, closing restores focus, and live updates preserve input drafts.
- More consistent native widget icons/materials and contrast-aware text on solid custom surfaces. Surface opacity remains independent from text. Long to-do items wrap while remaining editable.
- Two-row navigation and responsive canvas/cards for enlarged interface text. No continuous decorative animation.

Notes, tasks, Spaces, widget themes, data format 5 and update behavior are preserved. App identity/data paths are unchanged. Luma is still Beta; internal build numbers increase so installed updaters continue working.

## Get this update

Existing Windows Setup copies: open Settings → Check for updates in your current build. Once installed, the new layout places update controls in Settings → Updates. Downloaded updates install when you Quit Luma, or choose Restart to update. Closing the panel leaves Luma in the tray. Portable and Mac preview copies remain manual; the separate Mac 2.6 preview is unchanged.

## Verification and limits

51 unit tests, packaged UI/refinement checks, default/populated captures of all sixteen real native widgets, three core themes, 1000/1600px windows and 100/125/150% renderer zoom, dialog/keyboard/long-content flows and exact saved-state restoration. Native OS movement/toolbar/Spaces and updater checksum/download/handoff regressions are verified separately.

Renderer zoom is not a physical mixed-DPI test. Physical display changes, sleep/resume, Explorer/fullscreen combinations and full installer replacement remain unverified. OS-native menu/notification appearance was not captured. Arbitrary wallpaper colors beneath translucent custom midtone surfaces can affect perceived contrast. Windows builds are unsigned. Actual idle samples are observations, not a performance guarantee.
