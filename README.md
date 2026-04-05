# ✍️ PDF Sign Here Stamp
### by [Midas Tech Inc.](https://www.midastech.ca) — IT Services & Cybersecurity

A professional PDF signing tool that automatically places **"Sign Here"** arrow stamps on client documents. No server, no install, no subscription — runs entirely in your browser.

**🔗 Live App:** [https://midastechinc.github.io/PDF-Signhere-Stamp/](https://midastechinc.github.io/PDF-Signhere-Stamp/)

**📦 Repository:** [https://github.com/midastechinc/PDF-Signhere-Stamp](https://github.com/midastechinc/PDF-Signhere-Stamp)

---

## Features

| Feature | Details |
|---|---|
| 📋 **Template System** | Save stamp layouts per document type (MSA, NDA, SLA…). Auto-applies on future uploads. |
| 🖱️ **Click to Place** | Click anywhere on the live PDF preview to drop a stamp. Drag to reposition. |
| ↔️ **Resize Stamps** | Drag the corner handle or use the sidebar slider to resize any stamp. |
| 🔍 **Auto-Detect** | Scans for signature lines (`______`) and keywords like "Signature:", "Sign Here" automatically. |
| 📁 **Batch Processing** | Drop a whole folder of PDFs — matched templates are stamped in one click. |
| 💾 **Save to Folder** | Use the OS folder picker to save stamped PDFs directly to any folder on your PC. |
| 📤 **Template Export/Import** | Export templates as `mt_templates.json` to share across machines or back up. |
| 🔒 **100% Local** | No data leaves your browser. PDFs are never uploaded to any server. |

---

## How to Use

### Single Document
1. Open the app and drag & drop a PDF onto the left panel
2. Click anywhere on the document preview to place a **Sign Here** stamp
3. Drag stamps to reposition · Use corner handle to resize
4. Click **💾 Save Template** and name it (e.g. "MSA Agreement")
5. Click **⬇ Download PDF** to get the stamped file

### Batch Processing
1. Switch to the **📁 Batch Folder** tab
2. Drop a folder of PDFs (or click to select multiple files)
3. Files with matching templates show ✓ green — others show ⚠ No match
4. Click **📁 Set Folder for All** to pick where stamped files are saved
5. Click **▶ Process All** → **📦 Download All**

### Templates
- Templates are saved in your browser's localStorage automatically
- Click **📤 Export** to download `mt_templates.json` — save it to `C:\Document_StampFolder\`
- On any machine, click **📥 Import** and load that file to restore all templates
- Tick **Auto-export** to keep the JSON updated every time you save a new template

---

## Browser Requirements

| Browser | Single Doc | Batch | Folder Save |
|---|---|---|---|
| Chrome 86+ | ✅ | ✅ | ✅ |
| Edge 86+ | ✅ | ✅ | ✅ |
| Firefox | ✅ | ✅ | ⚠️ Downloads only |
| Safari | ✅ | ✅ | ⚠️ Downloads only |

> **Folder Save** (direct-to-folder output) requires the File System Access API, available in Chrome and Edge only.

---

## Hosting — GitHub Pages Setup

This repo is already configured for GitHub Pages. To activate:

1. Go to **Settings → Pages**
2. Set Source: **Deploy from branch → `main` → `/ (root)`**
3. Click **Save**
4. Live in ~60 seconds at: **https://midastechinc.github.io/PDF-Signhere-Stamp/**

---

## Project Structure

```
PDF-Signhere-Stamp/
├── index.html          ← The entire application (self-contained)
├── README.md           ← This file
├── LICENSE             ← MIT License
├── .gitignore          ← Git ignore rules
└── .github/
    └── CODEOWNERS      ← Repo ownership
```

The entire app is a single self-contained HTML file. All PDF processing libraries (pdf.js, pdf-lib) are loaded from CDN. No build step, no npm, no dependencies to install.

---

## Updating the App

When a new version is ready:

**Via GitHub web UI (no Git needed):**
1. Go to the repo → click `index.html`
2. Click the ✏️ pencil icon → select all → paste new content
3. Click **Commit changes** — live in ~30 seconds

**Via Git:**
```bash
git add index.html
git commit -m "Update app to latest version"
git push origin main
```

---

## Sharing with Your Team

- **Bookmark:** `https://midastechinc.github.io/PDF-Signhere-Stamp/`
- **Templates:** Share `mt_templates.json` via email or shared drive so everyone starts with the same stamp layouts
- **Desktop shortcut:** In Chrome → ⋮ → *Save and share → Create shortcut → Open as window* — runs like a desktop app

---

## Tech Stack

- **[PDF.js](https://mozilla.github.io/pdf.js/)** — PDF rendering and text extraction
- **[pdf-lib](https://pdf-lib.js.org/)** — PDF modification and stamp embedding
- **File System Access API** — Direct folder read/write (Chrome/Edge)
- **localStorage** — Template persistence across sessions
- Vanilla HTML/CSS/JS — Zero framework dependencies

---

## Privacy & Security

- ✅ All PDF processing happens **client-side in your browser**
- ✅ No files are uploaded to any server
- ✅ No analytics, no tracking, no ads
- ✅ Templates stored locally in your browser only
- ✅ Works offline after first load (CDN libraries cached by browser)

---

## About Midas Tech Inc.

**Midas Tech Inc.** is a Managed Service Provider (MSP) based in Richmond Hill, Ontario, Canada, serving SMBs in healthcare, accounting, and logistics.

📧 info@midastech.ca | 📞 905-787-2038 | 🌐 [midastech.ca](https://www.midastech.ca)  
30 Via Renzo Dr, Suite 200, Richmond Hill, ON L4S 0B8

---

## License

MIT License — free to use, modify, and distribute.
