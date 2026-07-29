# MD3 Markdown Viewer (Chrome Extension)

This is a Manifest V3-compatible Chrome extension that, when you open a local Markdown file (`file:///*.md`) in the Chrome browser, overrides the browser’s standard, plain-text display and dynamically replaces it with a beautiful Markdown preview screen compliant with Material Design 3 (MD3).

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![MV3](https://img.shields.io/badge/manifest-v3-green.svg)

---

## 🌟 Key Features

*   **MD3-Compliant Premium Design**: 
    A beautiful, easy-on-the-eyes document environment based on the Material Design 3 color palette (with a focus on dark themes).
*   **Glass Morphism Header**: 
    The Top App Bar at the top of the screen uses `backdrop-filter` to apply transparency and blur effects, allowing content to show through beautifully as you scroll.
*   **Hierarchical Accordion-Style Table of Contents (TOC)**:
    Automatically analyzes headings (H1–H3) in the main text and dynamically generates a tree-structured table of contents with parent-child relationships in the left sidebar. Each item can be collapsed or expanded.
*   **Intelligent ScrollSpy (Automatic Scroll Tracking)**:
    As the main content is scrolled, a purple vertical slide-in indicator accurately and smoothly tracks the current position (active item) in the table of contents. Additionally, if the active item is located within a collapsed level, the parent level is automatically expanded.
*   **Sliding the Table of Contents (Sidebar) Open and Closed**:
    You can slide the sidebar to the left to hide it by clicking the table of contents header or the menu button (three horizontal lines) in the upper-left corner. When the sidebar is closed, the main content area smoothly expands to full screen width, allowing you to read the document comfortably.
*   **Breadcrumb Trail**:
    It analyzes the absolute path of local files and generates navigation links at the top of the screen that let you return to the parent directory with a single click.
*   **Switching Between Preview and Plain Modes**:
    Using the segmented button in the header, you can easily switch between the formatted “Preview” (document view) and raw Markdown “Plain” (text view).
*   **Various Copy Functions and Toast Notifications (Snackbar)**:
    You can copy the entire raw Markdown or individual code snippets within code blocks with a single click. When copying is successful, an MD3-compliant Snackbar pops up from the bottom of the screen to notify you that the operation is complete.

---

## 📂 File Structure

```text
chrome-md3-markdown-viewer/
├── manifest.json          # Extension configuration file (MV3 compatible)
├── content.js             # Retrieves plain text from MD files, builds the overall UI, and controls interactions
├── marked.min.js          # Lightweight library for parsing Markdown into HTML (included)
├── styles.css             # MD3-based UI styling (table of contents, breadcrumbs, preview)
├── sample.md              # Sample Markdown file for testing
├── README.md              # This file
└── icons/                 # Extension icon images (MD3 design)
    ├── icon16.png
    ├── icon48.png
    └── icon128.png
```

---

## 🚀 Installation Instructions (Installation in Developer Mode)

These are the steps to install the extension directly into Chrome from your local development code, without going through the Chrome Web Store.

1.  Save the source code from this repository to your local environment.
2.  Open Google Chrome, enter `chrome://extensions/` in the URL bar, and open the Extensions page.
3.  Toggle the “**Developer Mode**” switch in the top-right corner of the screen to **On**.
4.  Click the “**Load unpacked extension**” button displayed in the top-left corner of the screen.
5.  A file selection dialog will appear; select the root directory of this project (`chrome-md3-markdown-viewer`) and load it.
6.  **[Important]** Click the “**Details**” button on the loaded extension card, and set the “**Allow access to file URLs**” toggle switch at the bottom of the settings page to **On**.
    *   *Note: If you do not configure this setting, the extension will not work with Markdown files on the local `file://` scheme.*

---

## 📝 How to Use

1.  In the Chrome browser, open any local `.md` (or `.markdown`) file (you can also open a file by dragging and dropping it into the browser).
2.  The screen will automatically switch to MD3’s beautiful preview view.
3.  To check the display, drag and drop the included `sample.md` file into Chrome to test how it works.

---

## License

[MIT License](LICENSE)
