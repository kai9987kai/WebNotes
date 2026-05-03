# Advanced Enhanced Notes Application v2

A polished, privacy-friendly, local-first browser notes application built as a single HTML file. It combines rich text editing, note organisation, fast search, drag-and-drop ordering, local autosave, import/export tools, and a modern responsive interface.

## Overview

Advanced Enhanced Notes v2 is designed for quick personal note-taking without requiring a server, database, account, or build process. Everything runs directly in the browser and stores notes in `localStorage`, making it simple to open, use, back up, and customise.

The app keeps the original note-taking features while adding a more powerful workspace for organising, editing, exporting, and managing notes over time.

## Key Features

### Rich Text Editor

* Bold, italic, underline, and strikethrough formatting
* Font family selector
* Font size selector
* Text colour picker
* Bullet and numbered lists
* Link insertion
* Clear formatting button
* Contenteditable writing area
* Sparkle typing effect
* Live word count, character count, and reading-time estimate

### Notes Management

* Create notes with titles
* Save notes locally in the browser
* Edit notes inline
* Delete individual notes
* Clear all notes with confirmation
* Drag and drop notes to reorder them in manual sort mode
* Timestamps for created and updated dates
* Automatic migration from the older `localStorage` key used by the original app

### Organisation Tools

* Tags for notes
* Tag filtering
* Tag cloud sidebar
* Pinned notes
* Favourite notes
* Archive and restore notes
* Note colour themes
* Multiple view filters:

  * All active notes
  * Pinned notes
  * Favourite notes
  * Archived notes

### Search and Sorting

* Search across note titles, note body text, and tags
* Search result highlighting
* Sort by:

  * Manual order
  * Recently updated
  * Newest created
  * Oldest created
  * Title A-Z
  * Most words

### Backup and Portability

* Export all notes as JSON
* Import notes from JSON
* Export notes as a readable HTML document
* Merge imported notes or replace the current notebook

### Interface Enhancements

* Modern responsive layout
* Dark mode and light mode
* Focus mode for distraction-free writing
* Notebook statistics sidebar
* Mobile-friendly design
* Toast notifications
* Keyboard shortcut: `Ctrl/Cmd + S` to save

### SEO and Metadata

* Dynamic meta description generation
* Dynamic keyword generation
* JSON-LD structured data for the web application

## How to Use

1. Save the HTML file to your computer.
2. Open it in a modern browser such as Chrome, Edge, Firefox, or Safari.
3. Type a title, optional tags, and your note content.
4. Use the toolbar to format your note.
5. Click **Save Note** or press `Ctrl/Cmd + S`.
6. Search, sort, tag, pin, favourite, archive, or reorder notes as needed.
7. Export JSON regularly if you want a backup.

## Data Storage

The app stores notes in browser `localStorage` using the key:

```txt
advancedNotes.v2.notes
```

Draft content is stored under:

```txt
advancedNotes.v2.draft
```

Theme preference is stored under:

```txt
advancedNotes.v2.theme
```

The app can also migrate older notes stored under the previous key:

```txt
notes
```

Because `localStorage` is browser-specific, notes saved in one browser or device will not automatically appear in another. Use JSON export/import to move or back up notes.

## Import and Export

### Export JSON

Use **Export JSON** to download a complete backup of your notes. This is the best format for restoring notes later.

### Import JSON

Use **Import JSON** to load a previous backup. The app will ask whether to merge imported notes with your current notes or replace the current notebook.

### Export HTML

Use **Export HTML** to create a readable standalone document containing your notes. This is useful for sharing, printing, or archiving, but JSON is better for restoring editable data.

## Keyboard Shortcuts

| Shortcut               | Action                              |
| ---------------------- | ----------------------------------- |
| `Ctrl + S` / `Cmd + S` | Save the current note               |
| `Ctrl + B` / `Cmd + B` | Browser rich-text bold command      |
| `Ctrl + I` / `Cmd + I` | Browser rich-text italic command    |
| `Ctrl + U` / `Cmd + U` | Browser rich-text underline command |

## Project Structure

This is a single-file app. Everything is contained in one HTML document:

```txt
index.html
```

The file includes:

* HTML structure
* CSS styling
* JavaScript functionality
* SEO enhancement script

No external dependencies are required.

## Browser Compatibility

The app should work in modern desktop and mobile browsers that support:

* `contenteditable`
* `localStorage`
* `FileReader`
* `Blob`
* Drag and drop events
* Modern CSS grid and flexbox

Recommended browsers:

* Google Chrome
* Microsoft Edge
* Firefox
* Safari

## Privacy

This app is local-first. Notes are saved in your browser and are not sent to a server by the app.

However, browser data can be cleared manually or by browser privacy tools. Export your notes as JSON if they are important.

## Customisation Ideas

Possible future improvements include:

* Markdown export
* PDF export
* Password-protected encrypted notes
* Note folders or notebooks
* Reminder dates
* Checklist mode
* Image attachments
* Full-text fuzzy search
* Service worker support for installable PWA behaviour
* Cloud sync through an optional backend
* Version history for notes
* Recycle bin for deleted notes

## Known Limitations

* Notes are stored only in the current browser profile.
* Clearing site data may delete notes.
* `document.execCommand()` is widely supported but considered legacy in modern web standards.
* Drag reordering is intended for manual sort mode only.
* HTML export is readable, but JSON export is the recommended backup format.

## Development Notes

The app intentionally avoids frameworks and build tools so it remains portable and easy to edit. You can customise the design by editing the CSS variables in the `:root` section.

Important CSS variables include:

```css
--bg
--surface
--text
--muted
--accent
--accent-2
--danger
--radius
```

Core JavaScript areas include:

* Note creation and saving
* Draft autosave
* Rendering and filtering
* Tag management
* Import/export
* Theme handling
* Inline editing
* Drag-and-drop ordering

## Suggested File Name

```txt
advanced-enhanced-notes-v2.html
```

## License

You can use, modify, and share this project freely for personal or educational purposes. Add your preferred license if publishing it publicly.
