# font-provenance

**Dated, source-verified timelines of bundled fonts and default-typeface changes — for dating documents and fingerprinting the software that made them.**

A document set in Calibri cannot honestly predate 2006-05-23. A PDF whose text renders in Adobe Sans MM went through Acrobat with its fonts missing. A Simplified-Chinese body in 等线 (DengXian) cannot predate 2015-07-29. This repository assembles the release-dated evidence behind such reasoning, across operating systems (Windows, macOS, iOS, Android, desktop Linux — including per-script CJK lanes for Simplified Chinese, Traditional Chinese, Hong Kong, Japanese, and Korean), office suites (Microsoft Office and its East Asian editions, OpenOffice/LibreOffice, WPS Office, Google Docs, Apple iWork, Ichitaro, Hancom), PDF and scan/OCR tooling (Acrobat, PaperPort and peers), and document-generation libraries (Aspose and peers).

## Layout

- [`paper/`](paper/) — the citable artifact: a two-column XeLaTeX + xeCJK paper (`font-provenance.tex`/`.bib`, built PDF committed). Build with `make` inside `paper/` (requires a TeX distribution with XeLaTeX and the macOS CJK fonts Songti TC, Hiragino Mincho ProN, Apple SD Gothic Neo). See [`paper/README.md`](paper/README.md).
- [`docs/font-provenance-timelines.md`](docs/font-provenance-timelines.md) — the research register: the same content in markdown with hotlinked citations and per-citation verification tiers ([verified live] / [archive] / [secondary] / UNCERTAIN). This is the verification trail behind every claim in the paper.

## Method, in one paragraph

Every event is cited to the most authoritative source located (vendor documentation, press releases, project records, institutional archives, first-person designer accounts), each citation was fetch-verified against its claim during the July 2026 research window, dead originals fall back to Internet Archive snapshots, and anything that could not be adequately verified is labeled UNCERTAIN rather than asserted. The paper's §2 states the protocol and the evidence-tier semantics; §8 states the limitations. Drafts were adversarially reviewed by an independent model critic (two passes), and all 208 cited URLs were swept for liveness.
