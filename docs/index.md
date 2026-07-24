# font-provenance

**Dated, source-verified timelines of bundled fonts and default-typeface changes — for dating documents and fingerprinting the software that made them.**

A document set in Calibri cannot honestly predate 2006-05-23. A PDF whose text renders in Adobe Sans MM went through Acrobat with its fonts missing. A Simplified-Chinese body in 等线 (DengXian) cannot predate 2015-07-29. This project assembles the release-dated evidence behind such reasoning.

## Coverage

- **Operating systems** — Windows, macOS, iOS, Android, desktop Linux, each with per-script CJK lanes (Simplified Chinese, Traditional Chinese, Hong Kong, Japanese, Korean)
- **Office suites** — Microsoft Office (including East Asian edition defaults), OpenOffice/LibreOffice, WPS Office, Google Docs, Apple iWork, JustSystems Ichitaro, Hancom Office
- **PDF and scan/OCR tools** — Adobe Acrobat/Reader substitution fonts (Base-14, Adobe Sans/Serif MM, Minion Pro, the CJK Std packs), PaperPort, ABBYY FineReader, OmniPage, Readiris
- **Document-generation libraries** — Aspose.Words/Cells/Slides/PDF defaults and substitution chains, with peers (iText, openpyxl, python-docx)

## The artifacts

- **[The paper](https://github.com/SecurityRonin/font-provenance/blob/main/paper/font-provenance.pdf)** — a 26-page two-column XeLaTeX + xeCJK reference paper with per-platform timeline figures and a numbered bibliography carrying per-source verification tiers. Source and build in [`paper/`](https://github.com/SecurityRonin/font-provenance/tree/main/paper).
- **[The research register](font-provenance-timelines.md)** — the same content in markdown with hotlinked citations, each tagged `[verified live]` / `[archive]` / `[secondary]` / `UNCERTAIN`. This is the verification trail behind every claim.

## Method

Every event is cited to the most authoritative source located (vendor documentation, press releases, project records, institutional archives, first-person designer accounts). Each citation was fetch-verified against its claim during the July 2026 research window; dead originals fall back to Internet Archive snapshots; anything that could not be adequately verified is labeled UNCERTAIN rather than asserted. Drafts were adversarially reviewed by an independent model critic, and all cited URLs were swept for liveness. The paper's §2 states the protocol; §8 states the limitations.

---

[Privacy Policy](privacy.md) · [Terms of Service](terms.md) · © 2026 Security Ronin Ltd.
