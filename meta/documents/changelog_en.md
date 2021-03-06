## 0.4.1

### Fixed 

* **Case insensitive filesystem support:** On case-insensitive file systems, files (where only the case was changed) were deleted immediately after they were pulled. This has been fixed.

## 0.4.0

### New
* **User interface performance:** The user interface can now be operated smoothly while many files are synchronized.
* **German user interface:** The user interface has been translated to german.

### Fixed 

* **Non-closable success messages:** Success messages can now be closed as intended.
* **New plugins without ServiceProvider:** New plugins are now recognized even if no ServiceProvider is specified in plugin.json, because this is optional.
* **Windows certificate updated:** Users will not longer see a warning, if they use plentyDevTool on Windows for the first time. 

## 0.3.1

### Fixed

* **Unhandled Exception on malformed plugin zips:** the download of a plugin as zip file will sometimes fail. plentyDevTool can now handle it better and downloads the single files as a fallback.
* **Show not changed files as "modified" (MacOS):** MacOS sometimes changes the last modified timestamp of files when they are read-only. For this reason, MacOS now performs an additional content check to prevent files from being incorrectly displayed as "modified".
* **Multiple syncs (MacOS)** Under MacOS, the internal sync logic is no longer executed multiple times when the window is closed and reopened without closing the app completely (cmd + q) in the meantime.
* **No Push while building**: Changes are no longer pushed if a build process is already running in the system.

## 0.3.0

### New

* **Show current action details** Below the progress bar, the currently processed file is now displayed for a better understanding of the process.
* **Continuable Downloads** If a download is interrupted, the already written data will now be deleted and downloaded again at the next "pull".

### Fixed

* **Changes on same file remote and local** It is no longer attempted to rename a deleted file on pulling if the same file has also been modified remotely.
* **Error during ZIP extraction** If an error prevents unpacking plugins downloaded as ZIP files, the plugin files will now be downloaded individually.
* **Progress bar on Login** A progress bar is no longer displayed in the login screen if the app wants to log in with expired credentials.

## 0.2.0

### New 

* **Logger**: From now on a log file will be written.
* **Disallowed Characters in file paths** Files with not allowed characters in file path will not longer be pushed. Instead a warning displays a list of them.

### Fixed

* **Install new Plugin** Plugin directories must have the same name as the plugin. A bug in the check has been fixed.

## 0.1.0

### New

* **Auto update**: From now on, you will immediately know when we release a new version - plentyDevTool will tell you and give you the option to update right away.
* **Keyboard shortcuts**: You can now use a number of keyboard shortcuts: Cut (X), Copy (C), Paste (V), Select all (A), and Undo (Z) and forced quit (Q). The last one means Mac OS users no longer have to close the app via the taskbar.
* **Tooltips**: We added some tooltips to the buttons above the plugin set menu.

### Fixed

* **High CPU load on Windows and Linux**: We slowed down the watcher to reduce the load. It may take up to 3 seconds now for changed files to be displayed in the list.
* **File renaming bug on Windows**: There was a bug when making changes to the renamed file both locally and remotely. Is is now fixed.
* **Linux file watcher bug**: The file watcher was acting up on Linux systems and no longer does.

## 0.0.1
