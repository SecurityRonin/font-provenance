# Paper: Bundled Fonts and Default-Typeface Changes

A dated, sourced provenance reference for font-based document analysis: verified
timelines of default system/UI fonts and bundled-font milestones across Windows,
macOS, iOS, Android, and desktop Linux (with per-script CJK lanes — Simplified
Chinese, Traditional Chinese, Hong Kong, Japanese, Korean); default document fonts in
the major office suites (Microsoft Office and its East Asian editions,
OpenOffice.org/LibreOffice, WPS Office, Google Docs, Apple iWork, JustSystems
Ichitaro, Hancom Office); default and substitution fonts in PDF and scan/OCR tooling
(Adobe Acrobat/Reader, PaperPort and OCR peers); and default-font/substitution
behavior in document-generation libraries (the Aspose suites and peers). Every event
carries a hotlinked citation and an explicit verification tier; where sourcing is only
secondary or incomplete, the claim says so, and unverifiable claims are labeled
UNCERTAIN.

## Files
- `font-provenance.tex` — the paper source (XeLaTeX + xeCJK, two-column).
- `font-provenance.bib` — bibliography (one entry per source; the `note` field
  carries each source's verification tier verbatim).
- `font-provenance.pdf` — the built PDF.
- `Makefile` — build target (`PAPER = font-provenance`).

## Build
Requires a TeX distribution with XeLaTeX and BibTeX. The CJK content is set with
`xeCJK`, so the following fonts must be installed — all are macOS system fonts:

- **Songti TC** — main CJK font (covers Simplified and Traditional Chinese).
- **Hiragino Mincho ProN** — Japanese kana (e.g. 游ゴシック, メイリオ), via the `\ja{…}`
  macro.
- **Apple SD Gothic Neo** — Korean hangul (e.g. 맑은 고딕, 바탕, 함초롬바탕), via the
  `\ko{…}` macro.

On a non-macOS host, substitute an equivalent per-script font in the preamble
(`\setCJKmainfont`, `\newCJKfontfamily\japanesefont`, `\newCJKfontfamily\koreanfont`).

```sh
make            # xelatex -> bibtex -> xelatex x2
make clean      # remove build intermediates
```

The build is clean: no `Missing character` warnings for any CJK string, no
undefined-citation or undefined-reference warnings. The bibliography uses the plain
numeric `unsrt` style rather than `unsrtnat`, because the paper cites numerically and
`unsrtnat`'s a–z author-year disambiguation overflows past `z` with more than 26
same-author/same-year vendor-documentation entries (e.g. the many Microsoft Learn
font-family pages), which corrupts the `.bbl`. Numeric `[n]` citations render
identically.

## Timelines
Each platform/product section carries an Aeon-Timeline-style lane figure built from a
single reusable construct, `\fptimeline` (a coloured vertical spine with year nodes on
the left and event labels on the right). Every event line from the source register
appears in the corresponding figure; the ten timelines are referenced from their
section text.

## Provenance of the claims
Every dated event, citation, and verification tier in this paper is drawn from the
verification register at [`docs/font-provenance-timelines.md`](../docs/font-provenance-timelines.md).
That document is the single source of truth: it holds the per-event prose, the named
footnotes with their source URLs, and the `[verified live]` / `[archive]` /
`[secondary]` / `UNCERTAIN` tags that this paper reproduces in each bibliography entry's
`note` field. The load-bearing caveats — secondary-only sourcing, Wayback snapshots
confirmed to exist but not re-read, and claims that could not be adequately verified —
are preserved verbatim in the text and the `.bib`, and are summarized in the paper's
Limitations section.
