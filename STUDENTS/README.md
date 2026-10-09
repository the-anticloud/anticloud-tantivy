# Students — TANTIVY

**Project:** TANTIVY  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/quickwit-oss/tantivy  
**Pinned commit:** `45bbb16542f157a099585bc988ce7f06e7b4fd5a`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ef68d0fb8db9666bdfa7ebecbe7557b00385c881cff18214f4121b865652f51b`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `45bbb16542f157a099585bc988ce7f06e7b4fd5a`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `ef68d0fb8db9666bdfa7ebecbe7557b00385c881cff18214f4121b865652f51b`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
