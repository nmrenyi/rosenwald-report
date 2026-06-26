# Quantifying the Invisible: Women Doctors in the Rosenwald Guides (1887–1906)

**Subtitle:** LLM-based Structured Data Extraction from the Rosenwald Guides: Methods and Hybrid Evaluation

📄 **[Read the final report (PDF)](https://renyi.ch/reports/rosenwald.pdf)** — covers the whole project  
📝 **[Annotation framework preprint (arXiv)](https://arxiv.org/abs/2605.25781)** — covers the Double Triangle annotation methodology only

EPFL Semester Project — Ren Yi  
Supervisors: Mikhaël Moreau, Dre Amélie Puche, Pr. Jérôme Baudry

---

## Overview

This report presents methods for transforming scanned pages of the *Rosenwald Guides* — historical French medical directories (1887–1949) — into structured data. The work supports the [MEDIF project](https://www.epfl.ch/), which studies the professional trajectories of early women physicians in France and French-speaking Switzerland.

The pilot corpus covers 20 editions (1887–1906), comprising 4,116 pages listing physicians and related professions.

---

## Report Structure

| Chapter | File | Content |
|---|---|---|
| 1 — Introduction | `1-Introduction.tex` | Research motivation, challenges of historical OCR, and summary of contributions |
| 2 — Related Work | `2-related-work.tex` | Survey of traditional OCR, multimodal LLMs, hybrid OCR+LLM pipelines, and human-in-the-loop annotation |
| 3 — Dataset | `3-dataset.tex` | Description of the Rosenwald Guides, corpus construction, and layout challenges |
| 4 — Double Triangle Framework | `4-double-triangular.tex` | Proposed annotation methodology: two independent LLM systems + lightweight human review to create gold labels efficiently |
| 4.5 — Benchmark | `4.5-benchmark.tex` | Benchmark construction, model selection, image preprocessing ablation study, and quantitative results |
| 5 — Extraction Pipeline | `5-extraction-pipeline.tex` | Comparison of four extraction paradigms (OCR-only, MLLM image-only, MLLM image+OCR, text-only LLM on OCR output) and evaluation |
| 5.5 — Women Doctors | `5.5-women-doctors.tex` | Qualitative and quantitative analysis of extracted female doctor entries across the corpus |
| 6 — Conclusion | `6-Conclusion.tex` | Summary of findings, limitations, and directions for future work |

---

## Code and Data

| Resource | Repository |
|---|---|
| Double Triangle Annotation Framework | https://github.com/nmrenyi/double-triangle-annotation |
| Extraction Pipeline | https://github.com/nmrenyi/extraire-tesseract-openai |
| Rosenwald Benchmark | https://github.com/nmrenyi/rosenwald-benchmark |
| Extraction Results | https://github.com/nmrenyi/rosenwald-extraction |

---

## Building the PDF

Requires a LaTeX distribution with `latexmk` and `biber`.

```bash
latexmk -pdf main.tex
```
