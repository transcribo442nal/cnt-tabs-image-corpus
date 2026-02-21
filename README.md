# CNT Tabs Image Corpus

Source:
Wilhelm Schmitz  
*Commentarii Notarum Tironianarum*

PDF Source:
Internet Archive digitization (CNT.pdf)

## Scope

PDF pages 125–389 (inclusive)

These correspond to the Tabulae (Tabs) section of the work.

## Image Layers

### Raw Page Render
- 300 DPI PNG render
- 265 pages
- cnt_tabs/pages_raw/raw-125.png → raw-389.png
- pages_raw.sha256 included

### Column Crops
- Each page split into 4 equal vertical columns
- 1060 total column images
- cnt_tabs/columns/p###-c00.png → p###-c03.png
- columns.sha256 included

## Determinism

Rebuild command:pdftoppm -r 300 -f 125 -l 389 -png CNT.pdf cnt_tabs/pages_raw/raw

Column split:convert pXXX.png -crop 4x1@ +repage +adjoin pXXX-c%02d.png

SHA256 manifests ensure reproducibility and integrity.

---

This repository contains only image layers.
OCR, parsing, and indexing are handled in separate repositories.

