### Hi, I'm Wasabi 👋

Building local-first **AI Agent infrastructure**, **audit-grade RAG corpora**, **verifiable citation pipelines**, and **browser-local privacy tools** ([ZeroInk](https://zeroink.tidyuse.com)) in Rust & Python.

### Composable Evidence Loop

```text
1. sessfork       Chrome auth capture + pre-write redaction (0 focus theft)
      │
      ▼
2. XERJ + kbwall  Air-gapped Rust MCP · sub-5ms hybrid search · xerj:// URIs
      │
      ▼
3. claimcite      Zero-dep span & citation verification against source text
```

**Powered by clean-room Hugging Face models:** [xerj-bilingual-fin-law-384](https://huggingface.co/wasabihu/xerj-bilingual-fin-law-384) (`384d`, `MIT`) · [VeriCorpus-Reranker-0.6B](https://huggingface.co/wasabihu/VeriCorpus-Reranker-0.6B) (`Apache-2.0`)

### Featured Open Source

| Project | What it solves | Links |
| :--- | :--- | :--- |
| **[sessfork](https://github.com/wasabihu/sessfork)** | **Headless Chrome auth session bridge** — forks live Cookies & LocalStorage into AI agent browsers with pre-write redaction for XERJ ingest, zero window focus theft, zero runtime deps. | [v0.1.6](https://github.com/wasabihu/sessfork/releases/tag/v0.1.6) · [Guide](https://wasabihu.github.io/sessfork/) · [中文](https://github.com/wasabihu/sessfork/blob/main/README.zh-CN.md) |
| **[kbwall](https://github.com/wasabihu/kbwall)** | **Read-only Rust MCP firewall** — air-gapped local KB proxy for [XERJ](https://xerj.org) & ES-compatible engines (~1 MB, zero Tokio/TLS, `unsafe_code = "forbid"`), emitting canonical `xerj://` URIs with hybrid filter pushdown. | [v0.2.0](https://github.com/wasabihu/kbwall/releases/tag/v0.2.0) · [中文](https://github.com/wasabihu/kbwall/blob/main/README.zh-CN.md) |
| **[claimcite](https://github.com/wasabihu/claimcite)** | **Zero-dep citation & span verifier** — verifies whether claims and quotes match CrossRef, PubMed, arXiv, or local `xerj://` sources (CLI + MCP Server). | [v0.7.0](https://github.com/wasabihu/claimcite/releases/tag/v0.7.0) · [Docs](https://wasabihu.github.io/claimcite/) · [中文](https://github.com/wasabihu/claimcite/blob/main/README.zh-CN.md) |
| **[vericorpus](https://github.com/wasabihu/vericorpus)** | **Audit-grade RAG corpora & benchmarks** — SEC/HKEX financial, statutory & clinical tables, PDF table reconstructor, and CJK query adapter (zero-dep stdlib core, Apache-2.0). | [v0.1.0](https://github.com/wasabihu/vericorpus/releases/tag/v0.1.0) · [Form D](https://github.com/wasabihu/vericorpus/tree/main/examples/formd-sample-30d) · [Docs](https://github.com/wasabihu/vericorpus/blob/main/docs/ENGINEERING_PHILOSOPHY.md) |
| **[cairnkit](https://github.com/wasabihu/cairnkit)** | **Host-owned Python agent runtime** — the host owns identity and permissions; every write becomes a draft a human approves. | [Repo](https://github.com/wasabihu/cairnkit) |
| **[AKReport](https://github.com/wasabihu/AKReport)** | **A-share & HKEX report downloader** — batch downloads financial report PDFs locally for investment research & knowledge-base workflows. | [Repo](https://github.com/wasabihu/AKReport) |

### Live Tools

| Tool | What it does | Live |
| :--- | :--- | :--- |
| **[ZeroInk](https://zeroink.tidyuse.com)** | **Zero-upload PDF & DOCX redactor** — browser-local WebGPU/WASM 27-label PII detection, red-stamp/signature masking, 300 DPI pixel destruction, and hidden Word metadata scrubbing. | [Launch](https://zeroink.tidyuse.com) |
| **[TidyUse](https://tidyuse.com)** | **Local-first browser utilities** — fast, ad-free client-side tools that keep user files on-device. | [Visit](https://tidyuse.com) |

### Verified Open Corpora & Signed Packs

| Corpus / Pack | Coverage & Verification | License |
| :--- | :--- | :--- |
| **[SEC Form D 30-Day Signed Pack](https://github.com/wasabihu/vericorpus/tree/main/examples/formd-sample-30d)** | **Ed25519-signed SEC filing pack** — 3,685 deduplicated initial Form D notices (`2026-10-06` to `2026-11-04`, 3,577 CIKs), anchored with `sec_edgar_url` + XML SHA-256 and zero-dep `verify_pack.py`. | `SEC Public` / `Apache-2.0` |
| **[corpus-cn-statutes](https://github.com/wasabihu/corpus-cn-statutes)** | **Verbatim PRC statutes corpus** — 29 civil, commercial, company & capital-market laws split into 3,204 one-file-per-article Markdown docs with SHA-256 `MANIFEST.tsv`. | `CC0-1.0` |
| **[corpus-clinical-trials](https://github.com/wasabihu/corpus-clinical-trials)** | **Quantitative clinical-table corpus** — 55 trial outcome records (271 Markdown pipe tables) from NIH ClinicalTrials.gov v2 and Europe PMC JATS XML. | `US-gov PD` / `CC-BY-4.0` |

### Clean-Room Open Models (Hugging Face)

| Model | What it does | License |
| :--- | :--- | :--- |
| **[xerj-bilingual-fin-law-384](https://huggingface.co/wasabihu/xerj-bilingual-fin-law-384)** | **384d bilingual CJK/EN embeddings** — FP32/FP16 ONNX + native XERJ Candle `safetensors`, reaching 92.0% R@1 / 100% R@5 in XERJ `rc.105` hybrid search. | `MIT` |
| **[VeriCorpus-Reranker-0.6B](https://huggingface.co/wasabihu/VeriCorpus-Reranker-0.6B)** | **Clean-room bilingual reranker** — `Qwen3-Reranker-0.6B` fine-tune hitting 1.0000 Top-1 / MRR & 0.9833 StrictCal on 240 zero-leakage groups. | `Apache-2.0` |

---

*Focus areas: Rust & Python · Local-First AI Agents · MCP · Verified RAG & Corpora · Citation Verification · Browser-Local Privacy*
