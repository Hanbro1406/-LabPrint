# 🖨️ LabPrint — Smart Photo to PDF

> **Made with ♥ by Hanbro & AP**

A zero-dependency, browser-based tool that packs your lab screenshots into A4 pages with maximum space efficiency — then exports a **print-ready 300 DPI PDF**. Built specifically for BTech CSE students who need to print code and output for lab records.

---

## ✨ Features

- 📸 **Drag & drop upload** — supports PNG, JPG, WEBP, BMP; upload multiple files at once
- 🧠 **Smart auto layout** — strip-packing algorithm analyzes each image's aspect ratio and fills every row edge-to-edge, minimizing blank space
- 📐 **Multiple layout modes** — Auto (max efficiency), 1/2/3 Column, and 2×2 Grid
- 🎛️ **Adjustable margins & gaps** — fine-tune spacing with live sliders
- 👁️ **Live preview** — see the exact A4 layout on screen before exporting
- ⚡ **Efficiency score** — shows % of page area covered by images
- 📄 **300 DPI lossless PNG export** — sharp enough to read every character of code
- 🔢 **Drag to reorder** — rearrange images before generating layout
- 🚫 **No installs, no server, no account** — runs entirely in your browser

---

## 🚀 Usage

1. Open `lab-print.html` in any modern browser (Chrome recommended)
2. Drag & drop your screenshots onto the upload zone, or click **Choose Photos**
3. Reorder images by dragging thumbnails if needed
4. Adjust layout mode, margins, and gap settings
5. Click **👁 Preview Layout** to see the A4 arrangement
6. Click **⬇ Export PDF** — saves `lab-record.pdf` at 300 DPI

No internet connection required after the page loads (jsPDF and fonts are loaded from CDN on first open).

---

## 📁 Project Structure

```
labprint/
│
└── lab-print.html      # The entire app — single self-contained file
└── README.md           # You're reading this
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Vanilla HTML/CSS/JS | UI & layout engine |
| [jsPDF 2.5.1](https://github.com/parallax/jsPDF) | PDF generation |
| HTML5 Canvas API | High-res page rendering at 300 DPI |
| JetBrains Mono + Syne | Typography (Google Fonts) |

---

## 🧮 How the Layout Algorithm Works

LabPrint uses a **strip-packing** approach:

1. For each page, images are placed row by row from top to bottom
2. For each row, it tries grouping 1–5 images side by side
3. Images in a row are scaled to the **same height**, with widths proportional to their aspect ratios — so the row fills the full page width
4. The row height that maximizes vertical space usage is chosen
5. This repeats until the page is full, then a new page starts

This ensures **zero wasted horizontal space** and minimizes the number of pages used.

---

## 💡 Why this exists

Every CSE lab submission needs printed code + output screenshots. Most students:
- Print one screenshot per page → wastes 60–70% of each sheet
- Manually resize in Word → takes forever

LabPrint automates this in seconds with optimal packing.

---

## 📜 License

MIT — free to use, modify, and share.

---

*Made with ♥ by **Hanbro** & **AP***
