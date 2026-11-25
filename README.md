### Hi, I'm Wasabi 👋

Building local-first **AI Agent infrastructure**, **audit-grade RAG corpora**, **verifiable citation pipelines**, and **browser-local privacy tools** in Python & Rust.

### Composable Evidence Loop

```text
sessfork ──► XERJ + kbwall ──► claimcite
│            │                 └─ Zero-dep span & citation verification
│            └─ Air-gapped Rust MCP · sub-5ms hybrid search · xerj:// URIs
└─ Chrome auth capture + pre-write redaction (zero window focus theft)

Powered by clean-room Hugging Face models:
  xerj-bilingual-fin-law-384 (384d, MIT) · VeriCorpus-Reranker-0.6B (Apache-2.0)
```

### Featured Open Source

| Project | What it solves | Links |
| :--- | :--- | :--- |
| **[vericorpus](https://github.com/wasabihu/vericorpus)** | Audit-grade financial (SEC/HKEX), statutory & clinical-table corpora, PDF table reconstructor, CJK query adapter, and verifiable retrieval benchmarks (zero-dep stdlib core, Apache-2.0). | [v0.1.0](https://github.com/wasabihu/vericorpus/releases/tag/v0.1.0) · [Form D 30d Pack](https://github.com/wasabihu/vericorpus/tree/main/examples/formd-sample-30d) · [Philosophy](https://github.com/wasabihu/vericorpus/blob/main/docs/ENGINEERING_PHILOSOPHY.md) |
| **[kbwall](https://github.com/wasabihu/kbwall)** | Air-gapped, read-only Rust MCP firewall for [XERJ](https://xerj.org) & ES-compatible local KBs (~1 MB, zero Tokio/TLS, `unsafe_code = "forbid"`), emitting canonical `xerj://` evidence URIs with hybrid filter pushdown. | [v0.2.0](https://github.com/wasabihu/kbwall/releases/tag/v0.2.0) · [中文文档](https://github.com/wasabihu/kbwall/blob/main/README.zh-CN.md) |
| **[claimcite](https://github.com/wasabihu/claimcite)** | Zero-dependency citation & span verifier across CrossRef, PubMed, arXiv, and local `xerj://` evidence URIs — checks whether the source exists, matches the claim, and contains the quoted words (CLI + MCP Server). | [v0.7.0](https://github.com/wasabihu/claimcite/releases/tag/v0.7.0) · [Docs](https://wasabihu.github.io/claimcite/) · [中文文档](https://github.com/wasabihu/claimcite/blob/main/README.zh-CN.md) |
| **[sessfork](https://github.com/wasabihu/sessfork)** | Fork live Chrome auth sessions (Cookies + LocalStorage) into headless AI agent browsers with pre-write redaction for XERJ ingest — zero window focus theft, zero runtime dependencies. | [v0.1.6](https://github.com/wasabihu/sessfork/releases/tag/v0.1.6) · [Interactive Guide](https://wasabihu.github.io/sessfork/) · [中文文档](https://github.com/wasabihu/sessfork/blob/main/README.zh-CN.md) |
| **[cairnkit](https://github.com/wasabihu/cairnkit)** | A small Python agent runtime for business apps — the host owns identity & permissions, writes become drafts a person approves. | [Repo](https://github.com/wasabihu/cairnkit) |
| **[AKReport](https://github.com/wasabihu/AKReport)** | Batch download A-share & HK-share financial report PDFs locally for investment research & NotebookLM / knowledge-base workflows. | [Repo](https://github.com/wasabihu/AKReport) |
| **[grokbot-marketplace](https://github.com/wasabihu/grokbot-marketplace)** | Bilingual Chinese/English catalog of 90 Grok Bot templates with full-text search and Markdown export. | [Browse](https://wasabihu.github.io/grokbot-marketplace/) |

### Verified Open Corpora & Signed Packs

| Corpus / Pack | Coverage & Verification | License |
| :--- | :--- | :--- |
| **[SEC Form D 30-Day Signed Pack](https://github.com/wasabihu/vericorpus/tree/main/examples/formd-sample-30d)** | 3,685 deduplicated initial U.S. SEC EDGAR Form D notices (`2026-10-06` to `2026-11-04`, 3,577 unique CIKs, entity-level public fields only), anchored with `sec_edgar_url` + XML SHA-256, detached Ed25519 signature, and zero-dep `verify_pack.py`. | `SEC Public Filing` / `Apache-2.0` |
| **[corpus-cn-statutes](https://github.com/wasabihu/corpus-cn-statutes)** | 29 PRC civil, commercial, company & capital-market statutes split verbatim into 3,204 one-file-per-article Markdown documents with SHA-256 `MANIFEST.tsv`. | `CC0-1.0` |
| **[corpus-clinical-trials](https://github.com/wasabihu/corpus-clinical-trials)** | 55 quantitative clinical trial outcome records (271 Markdown pipe tables) from US NIH ClinicalTrials.gov v2 and Europe PMC Open Access JATS XML. | `US-gov PD (NLM)` / `CC-BY-4.0` |

### Clean-Room Open Models (Hugging Face)

| Model | What it does | License |
| :--- | :--- | :--- |
| **[xerj-bilingual-fin-law-384](https://huggingface.co/wasabihu/xerj-bilingual-fin-law-384)** | 384-dim bilingual (CJK/EN) financial, statutory & clinical embedding model (FP32/FP16 ONNX + native XERJ Candle `safetensors`), reaching 92.0% R@1 / 100% R@5 in XERJ `rc.105` native hybrid search. | `MIT` |
| **[VeriCorpus-Reranker-0.6B](https://huggingface.co/wasabihu/VeriCorpus-Reranker-0.6B)** | Clean-room bilingual financial/legal/clinical cross-encoder reranker (`Qwen3-Reranker-0.6B` fine-tune): 1.0000 Top-1 / MRR & 0.9833 StrictCal on 240 zero-leakage groups. | `Apache-2.0` |

### Live Tools

| Tool | What it does | Access |
| :--- | :--- | :--- |
| **[ZeroInk](https://zeroink.tidyuse.com)** | Browser-local PDF & DOCX physical redaction workbench — zero-upload WebGPU/WASM PII detection, red-stamp/signature masking, 300 DPI pixel destruction, and hidden Word revision/metadata scrubbing. | [zeroink.tidyuse.com](https://zeroink.tidyuse.com) |

---

*Focus areas: Local-First AI Agents · Verified RAG & Corpora · MCP · Citation Verification · Browser-Local Privacy · Python & Rust*
