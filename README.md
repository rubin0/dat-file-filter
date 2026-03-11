# 🎮 ROM DAT Filter

A single-file, offline HTML tool for searching, selecting, and exporting subsets of ROM entries from standard DAT files — compatible with formats used by **ClrMamePro**, **RomVault**, **Logiqx**, and similar ROM management utilities.

---

## Features

- **Drag & drop DAT loading** — load any `.dat` or `.xml` file directly in the browser
- **Live search** — type 2+ characters to instantly filter across `<game>`, `<machine>`, and `<software>` nodes
- **Manual curation** — add and remove individual ROM entries from your output list
- **Configurable output filename** — set a console name and optional top-N number (e.g. `top_100_nes.dat`)
- **Standards-compliant XML export** — preserves the original DAT header and root element attributes
- **Fully offline** — all parsing and export happens client-side; no data ever leaves your machine
- **Zero dependencies** — pure HTML + CSS + JavaScript, no frameworks or build tools

---

## Usage

### 1. Open the tool
Open `[rom_dat_filter.html](https://rubin0.github.io/dat-file-filter/)` in any modern browser (Chrome, Firefox, Edge, Safari).

### 2. Load a DAT file
Drag a `.dat` or `.xml` file onto the drop zone, or click to browse.  
The tool will parse the file and report how many ROM entries were found.

> Supports Logiqx-style XML with `<game>`, `<machine>`, or `<software>` root elements.

### 3. Configure output filename *(optional)*
| Field | Description | Example |
|---|---|---|
| Console name | Short identifier appended to the filename | `nes`, `snes`, `megadrive` |
| Top number | Numeric prefix for the filename | `100` → `top_100_nes.dat` |

If the top number is left empty, the filename will use `top_x_<console>.dat`.

### 4. Search and select ROMs
Type in the search box to find entries by name or description.  
Click a result row (or the **+ ADD** button) to add it to the export list.  
Already-added entries are marked with a ✓ and cannot be added twice.

### 5. Download the filtered DAT
Once your list is ready, click **⬇ DOWNLOAD FILTERED DAT**.  
The exported file contains:
- The original root element with all its attributes intact
- The original `<header>` block (if present)
- Only the ROM entries you selected

---

Released for personal use.
