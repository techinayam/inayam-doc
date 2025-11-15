# 📝 Advanced Notepad Editor Tool

A feature-rich, multi-tab text editor with autosave, undo/redo, search &
replace, sidebar file explorer, and **persistent LocalStorage support**.

------------------------------------------------------------------------

## Overview

The Advanced Notepad Editor allows users to create, edit, and manage
multiple documents in a clean, tab-based interface. Every file you
create is **automatically stored in LocalStorage**, which means your
notes remain saved even after closing or refreshing the browser ---
without requiring manual downloads.
 

------------------------------------------------------------------------

## Features

### Core Functionality

-   **Multi-Tab Editor**\
    Create, rename, switch between, and close tabs at any time.

-   **Persistent Auto-Save (LocalStorage)**\
    File contents are saved automatically on every keystroke.

-   **Automatic Session Restore**\
    When you reopen the app, all files and tabs are restored from
    LocalStorage.

-   **Undo / Redo Functionality**\
    Each tab maintains its own undo and redo history.

-   **Search & Replace**\
    Built-in search (find) and replace, including "Replace All".

-   **Modified File Indicator**\
    Tabs show a dot (`●`) when content is unsaved.

-   **Word / Character / Line Count**\
    Real-time editor statistics.

-   **Responsive Layout**\
    Works across desktop and mobile. 

------------------------------------------------------------------------

## LocalStorage File System

### How Saving Works

-   Files are saved continuously while typing.
-   A file is **never deleted automatically**.
-   Closing a tab does **not** remove the file from LocalStorage.
-   Files can only be deleted manually from the sidebar delete button.
 
### What Is Not Saved

To avoid JSON corruption: - undoStack\
- redoStack

These are reconstructed fresh on each load.

------------------------------------------------------------------------

## Sidebar File Manager

### Features

-   Displays a full list of saved files
-   Hover to reveal a **Delete** button
-   Click file → Opens in active tab
-   Delete removes file permanently from LocalStorage

### No Deletion on Tab Close

Closing a tab does **not** delete the file --- it stays available in the
sidebar until explicitly removed.

------------------------------------------------------------------------

## Loading Files

When the Notepad loads: 1. It fetches `notepad_files` from LocalStorage\
2. Rebuilds all file tabs\
3. Initializes fresh undo/redo stacks for each file\
4. Displays the last active file

------------------------------------------------------------------------

## Search & Replace

-   Find text inside current file\
-   Replace single match\
-   Replace all matches\
-   Case-sensitive & whole-word support (optional)

------------------------------------------------------------------------

## Keyboard Shortcuts

  Shortcut               Action
  ---------------------- ----------------
  **Ctrl + N**           Create new tab
  **Ctrl + W**           Close tab
  **Ctrl + F**           Search text
  **Ctrl + H**           Replace text
  **Ctrl + Z**           Undo
  **Ctrl + Shift + Z**   Redo

------------------------------------------------------------------------

## Error Handling

### Common Issues Handled Automatically

-   LocalStorage full
-   Corrupted file entries
-   Missing fields on load
-   Invalid tab states

### Validation

-   Pure JSON saved (no functions or closures)
-   Undo/redo trimmed to avoid memory overflow

------------------------------------------------------------------------

## Browser Compatibility

-   Chrome 60+
-   Firefox 55+
-   Safari 12+
-   Edge 79+
-   Mobile browsers supported

------------------------------------------------------------------------

## Notes & Best Practices

-   Keep filenames short for clean sidebar layout\
-   Avoid storing extremely large files (\>5MB) in LocalStorage\
-   Use sidebar delete option to free storage\
-   useTranslations allows multilingual editor support

------------------------------------------------------------------------

*Last updated: 2025*
