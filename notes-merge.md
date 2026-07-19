---
name: notes-merge
description: Merge multiple PDFs into a single landscape Remarkable-optimized study or journal notebook. Use when the user wants to combine course sections, journal workbooks, scanned handwriting, personal notes, or any mix of PDFs into one clean master file with section dividers and optional table of contents. Triggers on notes merge, combine PDFs, master notebook, Remarkable merge, journal merge, or similar.
---

# Notes Merge Skill

Create clean, landscape Remarkable-optimized master PDFs by combining multiple source documents while preserving existing content and handwriting.

## When to Use

- Combining course modules with personal journal pages
- Merging in-progress workbooks that already contain handwriting
- Adding scanned paper journal pages into a digital master
- Building a single Week / Section / Theme notebook from several PDFs
- Any time the user says "merge these", "make a master", or "combine into one file for Remarkable"

## Core Rules

1. **Always confirm the final order** with the user before merging.
2. **Preserve everything** — never strip or rewrite existing handwritten or typed content.
3. **Landscape letter** is the default page size (Remarkable-friendly).
4. **Add clear section divider pages** between major documents so the user can navigate easily on the tablet.
5. **Keep original page dimensions** when possible. If a source is portrait, convert carefully or keep as-is and note it.
6. **Output one clean PDF** with a descriptive filename (e.g. `WW_Week5_Master_Notebook.pdf`).
7. After creating the master, offer to also keep the individual source files.

## Standard Workflow

1. List every PDF currently available (artifacts + attachments).
2. Propose a logical order and ask for confirmation or changes.
3. Confirm whether to include large journal workbooks (especially if they already have handwriting).
4. Ask if a simple Table of Contents / cover page is wanted.
5. Perform the merge using `qpdf` or `pypdf` (prefer qpdf for reliability with mixed content).
6. Add divider pages between major sections.
7. Deliver the final PDF and report page count + order used.

## Divider Page Style

Create simple, clean divider pages that contain:
- Section title (large, centered)
- Source document name
- Optional short subtitle
- Page number range if useful

Keep dividers minimal so they don’t waste tablet space.

## Handling Special Cases

- **Already-written journals** (like the 61-page workbook): Always include if the user says so. Never recreate or clean the handwriting pages.
- **Scanned paper notes**: Treat as full pages. Do not attempt OCR unless the user specifically requests a searchable version.
- **Mixed orientations**: Prefer keeping original orientation. Note any portrait pages in the final summary.
- **Duplicates**: If the same content appears in two files (e.g. Grey Jedi Thoughts), ask which version to keep.

## Scripts

Use scripts in `scripts/` for repeated merge operations when they become stable. Until then, perform merges with direct `qpdf` or Python `pypdf` calls and document the exact command used.

## Evolution

This skill should grow as real usage reveals patterns (e.g. preferred naming conventions, automatic TOC generation, bookmark support, etc.). Update after every few real merges.
