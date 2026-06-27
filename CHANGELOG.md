# Changelog

## 1.2.0

- Added installed Windows app selection inside App targets, alongside the existing executable picker.
- Improved App, File, and Folder target selection with a selector row, inline Advanced path editing, and resolved/unresolved target indicators while keeping Website targets as URL inputs.
- Added installed Windows app icon resolution from the Windows Shell and best-effort Launch Layout positioning through native activation process matching.
- Fixed installed Windows app icon extraction to preserve transparency when the Windows Shell provides alpha data.
- Added curated organizational tile colors with theme-tuned subtle tinted surfaces; bundle colors are independent from child item colors, and child item colors are preserved when ungrouped.
- Automatically normalize targets copied with Windows "Copy as path" by trimming surrounding whitespace and removing one full-value pair of surrounding quotes.
- Kept bundle item cursors consistent with reorder mode so inner bundle items do not imply click launching while tiles are being reordered.
- Kept launch arguments unsupported; quoted command strings with arguments are not parsed or modified.

## 1.1.0

- Added an optional Minimize to system tray setting with tray Show and Quit actions.
- Kept Close as a normal app exit while tray behavior remains opt-in.

## 1.0.0

- Initial public release of Personal Launchpad for Windows.
- Added local JSON persistence for activities, settings, and cached icons under `%APPDATA%/PersonalLaunchpad`.
- Added app, file, folder, and website launch targets.
- Added activity creation, editing, deletion, delete confirmation, and trim-on-save validation.
- Added rich icon support with emoji, selected image files, website favicons, and extracted app icons.
- Added local icon caching and reference-aware cleanup for unused cached icon files.
- Added Windows startup setting.
- Added activity bundles with bundle editing, compact item launching, optional item names inside bundle tiles, item ungrouping, and in-dialog item reordering.
- Added reorder-mode tile merging into bundles and a temporary merge undo toast.
- Added a visible reorder-mode active indicator.
- Added lightweight drag feedback and a short confirmation pulse for item tab reordering.
- Improved icon resolution robustness by preventing competing icon source changes while resolution is active.
- Added item and bundle name length limits with trim-on-save validation and subtle character-count feedback.
- Prevented duplicate top-level bundle names while still allowing repeated activity and item names.
- Improved optional bundle item labels with larger desktop preview cells, one-line truncation, and menu-safe narrow-layout positioning.
- Improved bundle tile interaction states, Ctrl launch-all feedback, edit affordances, and Activity / Bundle / Item terminology.
- Added custom frameless window chrome with native-feeling window controls, drag-to-edge Snap behavior, and in-app product identity.
- Added appearance settings for Dark, Light, and System Default themes.
- Hid the PowerShell window used during app icon extraction.
- Fixed NSIS uninstall app-data cleanup for `%APPDATA%/PersonalLaunchpad`.
- Verified blank first-run behavior with no bundled activity data.
