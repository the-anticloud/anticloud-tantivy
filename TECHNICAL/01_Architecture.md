# Technical Architecture — TANTIVY

**Upstream:** [https://github.com/tantivy-search/tantivy](https://github.com/tantivy-search/tantivy)
**License:** MIT
**Category:** SEARCH_ENGINES
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Rust full-text search engine library

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local semantic search — no third-party embedding API
2. AIOSS append-only index change log for reproducible search results
3. AES-256 encryption for all indexed private documents
4. Single-binary search engine deployable on single server
5. Zero-cloud: all crawling, indexing, and ranking runs locally
6. GPU/CPU equalizer: dense retrieval on GPU, BM25 on CPU
7. Zero-telemetry: no query logging to third parties
8. Open search API: OpenSearch-compatible REST interface

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_tantivy.spec` or `go build -o tantivy`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |