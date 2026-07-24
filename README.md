# font-provenance

[![Docs](https://img.shields.io/badge/docs-securityronin.github.io-blue)](https://securityronin.github.io/font-provenance/)
[![Paper](https://img.shields.io/badge/paper-PDF%20(26%20pp)-b31b1b)](https://github.com/SecurityRonin/font-provenance/blob/main/paper/font-provenance.pdf)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Sponsor](https://img.shields.io/badge/sponsor-h4x0r-ea4aaa?logo=githubsponsors)](https://github.com/sponsors/h4x0r)

**Dated, source-verified timelines of bundled fonts and default-typeface changes — for dating documents and fingerprinting the software that made them.**

A document set in Calibri cannot honestly predate 2006-05-23. A PDF whose text renders in Adobe Sans MM went through Acrobat with its fonts missing. A Simplified-Chinese body in 等线 (DengXian) cannot predate 2015-07-29. This repository assembles the release-dated evidence behind such reasoning — the working method behind the "Fontgate" class of findings, generalized across four decades of platforms.

## What's inside

| Artifact | What it gives you |
|---|---|
| [`paper/font-provenance.pdf`](paper/font-provenance.pdf) | The citable reference: 26 pages, two-column XeLaTeX + xeCJK, per-platform timeline figures, numbered bibliography with per-source verification tiers |
| [`docs/font-provenance-timelines.md`](docs/font-provenance-timelines.md) | The research register: the same ~200 events with hotlinked citations, each tagged `[verified live]` / `[archive]` / `[secondary]` / `UNCERTAIN` |
| §7 of either | The quick-reference anchor table: 22 first-availability anchors, each typed (font release vs OS bundling vs default binding) for correct anachronism reasoning |

## Coverage

- **Operating systems** — Windows (1.0→11), macOS (System 1→Sequoia), iOS, Android, desktop Linux — default system-font lineages and bundled-font milestones, each with per-script CJK lanes (Simplified Chinese, Traditional Chinese, Hong Kong/HKSCS, Japanese, Korean)
- **Office suites** — Microsoft Office including the East Asian edition defaults (SimSun→DengXian, MS Mincho→Yu Mincho, PMingLiU's non-change), OpenOffice/LibreOffice, WPS Office, Google Docs, Apple iWork, JustSystems Ichitaro, Hancom Office
- **PDF and scan/OCR tools** — Acrobat's Base-14, Adobe Sans/Serif MM, Minion Pro, and CJK Std substitution fingerprints; PaperPort, ABBYY FineReader, OmniPage, Readiris
- **Document-generation libraries** — Aspose.Words/Cells/Slides/PDF defaults and substitution chains (the Times New Roman / Fanwood tells), with peers

## Building the paper

```sh
cd paper && make    # xelatex -> bibtex -> xelatex x2
```

Requires a TeX distribution with XeLaTeX and the macOS CJK fonts (Songti TC, Hiragino Mincho ProN, Apple SD Gothic Neo). The built PDF is committed, so building locally is optional. See [`paper/README.md`](paper/README.md).

## Trust, but verify

Every event is cited to the most authoritative source located — vendor documentation, press releases, project records, institutional archives, first-person designer accounts — and each citation was fetch-verified against its specific claim during the July 2026 research window, with Internet Archive fallbacks for dead originals. Claims that could not be adequately verified are labeled UNCERTAIN rather than asserted. Drafts survived three adversarial review passes by an independent model critic, and all 208 cited URLs were liveness-swept. The paper's §2 states the protocol and evidence-tier semantics; §8 states the limitations — read both before relying on any single anchor.

---

[Privacy Policy](https://securityronin.github.io/font-provenance/privacy/) · [Terms of Service](https://securityronin.github.io/font-provenance/terms/) · © 2026 Security Ronin Ltd
