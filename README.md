### Hi, I'm Wasabi 👋

Building **zero-bloat Rust infrastructure for local AI agents** — sub-megabyte, zero-Node.js / zero-Tokio MCP servers, authenticated browser & CDP bridges, air-gapped KB firewalls, verifiable RAG/citation pipelines, and browser-local privacy tools ([ZeroInk](https://zeroink.tidyuse.com)).

### Composable Evidence Loop

```text
sessfork (Rust CDP MCP) ──► XERJ + kbwall ──► claimcite
│                           │                 └─ Zero-dep span & citation verification
│                           └─ Air-gapped Rust MCP · sub-5ms hybrid search · xerj:// URIs
└─ Chrome/Edge auth capture + zero-Node.js Moli / Chromium (--cdp-url) MCP runtime
```

> **Verified `sessfork-mcp` Numbers** *(~816 KiB single Rust binary, zero Node.js, reproducible locally)*:
> - **`-90.7%` RAM (`226.3 MiB` vs `2,439.5 MiB`) & `2.76×` faster** on 12× Heavy-DOM (`1,775` nodes/tab) — independently reproduced by the [`lexmount/moli` team](https://github.com/lexmount/moli/discussions/3465#discussioncomment-19846839) (Apple M4 24 GB, 5-run medians).
> - **`-27.5%` RAM (`-747.8 MB`) & `1.54×` faster on identical `chrome-headless-shell`** via `--cdp-url` (`3.2 ms` vs `1,240.4 ms` cold `initialize`) — pure MCP wrapper savings without switching browser engines.
> - **`100/100` hot-reload soak** (`0.85 ms` p50, Rust wrapper pinned flat at `2.8 MB`), **`0` surviving orphans on `SIGKILL` / Win32 Job Object**, and **`14/14` live adversarial security probes** ([Benchmarks](https://github.com/wasabihu/sessfork/blob/main/docs/benchmarks.md) · [Security Audit](https://github.com/wasabihu/sessfork/blob/main/docs/security-report.md)).

**Powered by clean-room Hugging Face models:** [xerj-bilingual-fin-law-384](https://huggingface.co/wasabihu/xerj-bilingual-fin-law-384) (`384d`, `MIT`) · [VeriCorpus-Reranker-0.6B](https://huggingface.co/wasabihu/VeriCorpus-Reranker-0.6B) (`Apache-2.0`)

### Featured Open Source

| Project | What it solves | Links |
| :--- | :--- | :--- |
| **[sessfork](https://github.com/wasabihu/sessfork)** | **Zero-bloat Rust CDP MCP & Chrome auth session bridge** — forks live Cookies & LocalStorage (incl. Windows Chrome `v20` ABE via Companion Extension) into Moli pipe or any loopback Chromium/CEF (`--cdp-url`), zero window focus theft, zero Node.js. | [v0.2.1](https://github.com/wasabihu/sessfork/releases/tag/v0.2.1) · [Benchmarks](https://github.com/wasabihu/sessfork/blob/main/docs/benchmarks.md) · [Security Audit](https://github.com/wasabihu/sessfork/blob/main/docs/security-report.md) · [中文](https://github.com/wasabihu/sessfork/blob/main/README.zh-CN.md) |
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

### Upstream Contributions & Ecosystem

- **[xerj-org/xerj](https://github.com/xerj-org/xerj)** — **Rust search & RAG engine** (ecosystem partner for `kbwall` & `vericorpus`): snapshot `fsync` batching ([#3457](https://github.com/xerj-org/xerj/pull/3457)), unmapped sub-field query fix ([#3527](https://github.com/xerj-org/xerj/pull/3527)), and CJK statutory & clinical reference corpora merged into XERJ Hub ([#3372](https://github.com/xerj-org/xerj/pull/3372)).
- **[lexmount/moli](https://github.com/lexmount/moli)** — **Rust headless browser** (dual-engine runtime for `sessfork`): mouse event `click_count` fidelity ([#3470](https://github.com/lexmount/moli/pull/3470)).
- **[d2lang/d2](https://github.com/d2lang/d2)** — **Declarative diagramming language**: `prefers-reduced-motion` accessibility support for animated SVG connections ([#2976](https://github.com/d2lang/d2/pull/2976)).
- **[ruvnet/ruflo](https://github.com/ruvnet/ruflo)** — **Vector memory durability**: atomic `hnsw.metadata.json` writes with surfaced failure handling ([#5001](https://github.com/ruvnet/ruflo/pull/5001)).
- **[a-r-j/graphein](https://github.com/a-r-j/graphein)** — **Graph ML CLI**: built-in default configuration presets ([#521](https://github.com/a-r-j/graphein/pull/521)).

### Async Rust MCP & Agent-Infra Engagements

Building an AI browser, local agent sandbox, or MCP runtime and want to eliminate Node.js bloat, cold-start latency, orphan processes, or cross-context security gaps? I take on focused, **100% async** technical engagements across time zones (architecture specs, benchmarks, and merge-ready PRs via GitHub Issues/PRs and email — no live meetings required):

| Scope | Deliverable | Typical Cadence |
| :--- | :--- | :---: |
| **Rust MCP Slim-Down Sprint** | Replace a heavy Node.js / Python MCP wrapper with a `<1 MB` pure-Rust binary (cross-platform macOS/Linux/Windows CI + reproducible before/after benchmarks) | 1 week |
| **Browser / Sandbox CDP & Auth Integration** | Attach native Rust MCP over OS pipes, Win32 Job Objects, or loopback `--cdp-url` to Chromium / CEF / stealth engines with isolated contexts, zero-secret-echo tool surfaces, and an adversarial verification harness | 1–2 weeks |
| **Async Architecture & PR Retainer** | Ongoing Rust systems engineering, security boundary hardening, memory-soak & performance regression tracking, and direct PR delivery | Monthly |

**Contact (async text):** [`wasabi.net@gmail.com`](mailto:wasabi.net@gmail.com) or open a GitHub issue on any repository above.

---

*Focus areas: Zero-Bloat Rust MCP · Local-First AI Agents · Headless Browser / CDP Runtime · Security Verification · Audit-Grade RAG & Citations*
