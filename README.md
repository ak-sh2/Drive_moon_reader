# DriveRead PDF — Browser PDF Reader, Converter & Highlighter

A clean, Google Drive-style PDF reader and document converter that runs **100% in your browser** (zero backend server, zero login, full offline/local storage privacy).

## Core Features

1. **Open & Drag-and-Drop Multi-Format Files**
   - Supports native **PDF** files plus **TXT, MD, HTML, CSV, JSON, RTF, DOCX, and source code files** (`.js`, `.ts`, `.py`, `.java`, `.c`, `.cpp`, `.css`, `.sql`, `.sh`, `.xml`, `.yaml`, `.go`, `.rs`, etc.).
2. **In-Browser PDF Conversion**
   - Automatically converts any non-PDF text, Markdown, CSV, JSON, HTML, RTF, DOCX, or code file into a multi-page formatted PDF document right inside the browser (preserving headings, line breaks, bullet lists, and monospace code blocks) and opens it in the unified PDF reader.
3. **Smooth Whole-Page PDF Reader**
   - Natural whole-page scrolling with a thin, subtle scrollbar and a compact sticky toolbar.
   - Zoom in/out, **Fit to Width**, **Page Number Jump**, **In-Document Search** (with match counter and next/previous navigation), and automatic **Last Page Memory** per file.
   - Mobile-friendly touch text selection and two-finger pinch-to-zoom.
4. **6-Color Persistent Highlighter**
   - Popular highlight palette: **Yellow, Green, Blue, Pink, Orange, and Purple**.
   - Pick a color and select text to highlight immediately.
   - Click any existing highlight on a page to **change its color** or **remove it**.
   - All highlights persist automatically per file in your browser (`IndexedDB` + `localStorage` backup).
5. **3-Mode Export & Print (Download PDF, Inline Viewer & Native Print)**
   - **With highlight colors**: Exports/prints the full PDF with all colored highlight overlays baked into the pages.
   - **Without highlight colors (Plain)**: Exports/prints the clean original PDF without markings.
   - **Highlighted parts only**: Generates a dedicated PDF containing an **Extracted Highlights Digest** (grouped by page and color) followed only by the pages that contain highlights.
6. **Google Drive-Style Library View**
   - Grid and List view toggle, instant search filter by filename or format, file metadata badges (page count, resume page, highlight count), **Rename**, and **Delete**.
7. **Dark / Light Theme Toggle**
   - Instant theme switch in the top header with persistent preference storage.

## Hosting on GitHub Pages (Step-by-Step)

Because this application is packaged as a self-contained `index.html` with zero build step required, you can host it for free on **GitHub Pages** in under a minute:

### Option A: Web Upload (Fastest — No Terminal Needed)
1. Create a new repository on [GitHub](https://github.com/new) (e.g., `drive-pdf-reader`).
2. Unzip `drive-pdf-reader.zip` on your computer and drag-and-drop `index.html`, `README.md`, and `.gitignore` into your GitHub repository page, then click **Commit changes**.
3. In your repository on GitHub, go to **Settings** → **Pages** (in the left sidebar).
4. Under **Build and deployment** → **Branch**, select **`main`** and folder **`/ (root)`**, then click **Save**.
5. Wait ~60 seconds, then open your live web app at:
   `https://<your-github-username>.github.io/<your-repo-name>/`

> **Note:** Clicking `index.html` inside the GitHub repository file list only shows the raw HTML source code. Always use your `https://<username>.github.io/<repo>/` URL to run the live app.

### Option B: Push from Terminal (Pre-Initialized Git Repo Included)
This zip archive already contains an initialized Git repository on branch `main`:
```bash
unzip drive-pdf-reader.zip -d drive-pdf-reader
cd drive-pdf-reader
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```
Then enable **Settings → Pages → Branch: `main`** on GitHub.

## Local Usage
Simply double-click `index.html` to open it in Chrome, Edge, Firefox, or Safari, or serve the folder locally with `python3 -m http.server 8000`.
