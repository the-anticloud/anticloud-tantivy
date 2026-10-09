# Educators — TANTIVY

**Project:** TANTIVY  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/quickwit-oss/tantivy  
**Pinned commit:** `45bbb16542f157a099585bc988ce7f06e7b4fd5a`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ef68d0fb8db9666bdfa7ebecbe7557b00385c881cff18214f4121b865652f51b`  
**Date:** October 2026

## Teaching with TANTIVY

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `ef68d0fb8db9666bdfa7ebecbe7557b00385c881cff18214f4121b865652f51b` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
