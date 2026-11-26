# Changelog

## 1.0.5

- Fixed activity tiles scrolling behind the Spaces bar. The activity area now shows up to two complete rows with a separate scrollbar and smooth row snapping.
- Tuned mouse-wheel sensitivity for controlled row changes and faster movement during sustained scrolling.
- Kept Settings compact with a dedicated update view for release notes, downloads, and installation confirmation.
- Downloads continue while you use Launchpad; return to the update view when ready to install. Choosing Later keeps the downloaded update ready for the current session.
- Disabled update controls no longer react visually to clicks.


## 1.0.4

- Fixed native file, folder, executable-app and custom icon pickers appearing behind Launchpad with Always on Top enabled.

## 1.0.3

- Check for updates in Settings. Personal Launchpad also checks quietly in the background. You choose when to download and install each signed update.
- Turn on Always on Top in Settings to keep the Launchpad window above other windows. Your preference is saved.
- The global hotkey brings Launchpad into focus when you are in another app, restores it when hidden or minimized, and minimizes it or sends it to the tray when it already has focus.
- Windows releases now use a single x64 NSIS installer.

Upgrading from v1.0.2? Install the v1.0.3 EXE manually once. Future releases will be available through the in-app updater.

If you installed v1.0.2 using the MSI, quit Launchpad completely and back up the entire `%APPDATA%\PersonalLaunchpad` folder for each Windows account that uses the app. Uninstall the MSI in Windows Settings, then verify the data folder is still present. If it is missing, restore the backup with Launchpad closed. Run the NSIS EXE under the same Windows account and verify your activities, Spaces, settings and cached icons before removing the backup.

## 1.0.2

- Added Spaces for organizing activities into up to six named contexts, with migration of existing activities into a default Space.
- Added Space reordering, startup Space behavior, and cross-Space movement for whole tiles and bundle child items in Reorder Mode.
- Added a configurable Global Hotkey for summoning Personal Launchpad, defaulting to `Ctrl+Alt+Space`, with editable shortcut settings.
- Added single-instance support so launching Personal Launchpad again focuses the existing app window.
- Added Open to system tray startup behavior.
- Polished Settings organization for Windows, Shortcuts, Spaces, appearance, and bundle display preferences.
- Refreshed public README structure, screenshots, release documentation, and the generic demo profile.

## 1.0.1

- Added Quick Drop activity creation for files, folders, executable apps, and `.url` internet shortcuts.
- Enabled startup, minimize-to-tray, and bundle item names by default for new users while preserving existing saved settings.
- Added executable app launch arguments in Advanced, including conservative parsing for pasted quoted executable command lines. Installed Windows app IDs do not support arguments.
- Added File Advanced support for filesystem paths and URI/protocol links such as `obsidian://open?vault=Scratch`.
- Suppressed the default Chromium/WebView context menu in release builds.
- Improved Reorder Mode with bundle child movement, quick delete shortcuts, and tighter tile icon resize behavior.

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
- Added Reorder Mode with visible active state, lightweight drag feedback, tile merging into bundles, temporary merge undo, and cursor behavior that keeps bundle items from implying launch actions while reordering.
- Added Launch Layouts for whole-bundle launches with a visual layout editor and best-effort Windows positioning, including improved matching for installed app windows.
- Added custom frameless Windows chrome with native-feeling window controls, drag-to-edge Snap behavior, centered startup, and in-app product identity.
- Added Dark, Light, and System Default appearance settings.
- Added launch-at-startup behavior and Minimize to system tray behavior with tray Show and Quit actions; startup, minimize-to-tray, and bundle item names default on for new users while existing saved settings are preserved.
- Automatically normalizes targets pasted from Windows "Copy as path" by trimming surrounding whitespace and removing one full-value pair of surrounding quotes.
- Fixed NSIS uninstall app-data cleanup for `%APPDATA%/PersonalLaunchpad`.
- Verified blank first-run behavior with no bundled activity data.
