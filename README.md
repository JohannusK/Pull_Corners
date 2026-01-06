# Pull Corners – Browser-Based Document Flattening

**Live tool:**  
👉 https://johannusk.github.io/Pull_Corners/

A **browser-based tool** for manually flattening photographed documents  
(e.g. fragile archive reports, books, scanned pages) by *pulling the corners*  
and exporting high-quality images or a combined PDF.
Everything runs locally in your browser.

---

## Why this exists

When working with fragile archive material, you are often:

- not allowed to scan
- forced to take photos at awkward angles
- required to preserve the **original visual appearance**
- unable to rely on automatic edge detection

This tool gives you **full manual control** over page geometry, while keeping the workflow fast and reproducible.

---

## Features

- 📂 Open one or multiple image files (local only, memory-only)
- 🔧 Manually select and adjust the four page corners
- 🖱️ Mouse + keyboard fine control
- 🔍 Zoomed-in view for precise alignment
- 📄 Perspective correction (“flattening”) with no additional processing
- 📐 Portrait / Landscape output toggle
- 🖼️ Download flattened JPG for the current page
- 📚 Export **image-only PDF** (visual fidelity preserved)
- 🌐 Works directly in the browser (GitHub Pages)

**What it does NOT do:**
- No automatic cropping or enhancement
- No OCR
- No compression tricks beyond standard JPEG encoding

---

## Quick start

1. Open the live tool:  
   👉 https://johannusk.github.io/Pull_Corners/
2. Click **Open images**
3. Adjust the four corner points
4. Press **Enter** to preview
5. Press **Enter** again to download the flattened image  
   or click **Download PDF** to export all pages

---

## Intended workflow

1. Take photos of pages (phone or camera)
2. Open the tool (locally or via GitHub Pages)
3. Adjust the four corners for each page
4. Export:
   - individual `*_flat.jpg` files, or
   - a combined PDF
5. *(Optional)* Run OCR later using a desktop tool (recommended)

Example OCR pipeline:
```bash
img2pdf *_flat.jpg -o report_raw.pdf
ocrmypdf --optimize 0 report_raw.pdf report_ocr.pdf
