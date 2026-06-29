# Changelog

## 1.0.1

- Added Quick Drop activity creation for files, folders, and executable apps.
- Enabled startup, minimize-to-tray, and bundle item names by default for new users while preserving existing saved settings.
- Added executable app launch arguments in Advanced, including conservative parsing for pasted quoted executable command lines. Installed Windows app IDs do not support arguments.
- Added File Advanced support for filesystem paths and URI/protocol links such as `obsidian://open?vault=Scratch`.
- Suppressed the default Chromium/WebView context menu in release builds.
- Improved reorder mode with bundle child movement, quick delete shortcuts, and tighter tile icon resize behavior.

## 1.0.0

- First binary-only public release of Personal Launchpad for Windows.
- Added local-first activity storage for apps, installed Windows apps, files, folders, websites, bundles, settings, and cached icons under `%APPDATA%/PersonalLaunchpad`.
- Added a redesigned target selection workflow for App, File, and Folder activities with selector rows, inline Advanced path editing, and resolved/unresolved target indicators while keeping Website targets focused on URL entry.
- Added installed Windows app support, including app picking, native activation, icon resolution from the Windows Shell, and improved installed-app icon transparency.
- Added activity creation, editing, deletion, delete confirmation, trim-on-save validation, name length limits, duplicate bundle-name prevention, and subtle character-count feedback.
- Added quick drag-and-drop activity creation for files, folders, and executable apps onto empty launchpad space.
- Added rich icon choices with emoji, selected image files, website favicons, extracted app icons, local icon caching, reference-aware cleanup, and safeguards against competing icon resolution updates.
- Added curated tile colors for activities and bundles with theme-aware tinting; bundle colors remain independent from child item colors, and child item colors are preserved when ungrouped.
- Added activity bundles with bundle editing, compact item launching, optional item labels, item reordering, item ungrouping, clearer Activity / Bundle / Item terminology, and polished bundle tile interactions.
- Added reorder mode with visible active state, lightweight drag feedback, tile merging into bundles, temporary merge undo, and cursor behavior that keeps bundle items from implying launch actions while reordering.
- Added Launch Layouts for whole-bundle launches with a visual layout editor and best-effort Windows positioning, including improved matching for installed app windows.
- Added custom frameless Windows chrome with native-feeling window controls, drag-to-edge Snap behavior, centered startup, and in-app product identity.
- Added Dark, Light, and System Default appearance settings.
- Added launch-at-startup behavior and Minimize to system tray behavior with tray Show and Quit actions; startup, minimize-to-tray, and bundle item names default on for new users while existing saved settings are preserved.
- Automatically normalizes targets pasted from Windows "Copy as path" by trimming surrounding whitespace and removing one full-value pair of surrounding quotes.
- Keeps launch arguments unsupported by design; quoted command strings with arguments are not parsed or modified.
- Fixed NSIS uninstall app-data cleanup for `%APPDATA%/PersonalLaunchpad`.
- Verified blank first-run behavior with no bundled activity data.
