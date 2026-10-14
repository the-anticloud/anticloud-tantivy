# Ethics — TANTIVY

**Project:** TANTIVY  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/quickwit-oss/tantivy  
**Pinned commit:** `45bbb16542f157a099585bc988ce7f06e7b4fd5a`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `ef68d0fb8db9666bdfa7ebecbe7557b00385c881cff18214f4121b865652f51b`  
**Date:** October 2026

## Position

TANTIVY is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
