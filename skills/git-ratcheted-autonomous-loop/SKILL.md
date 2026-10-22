---
name: git-ratcheted-autonomous-loop
description: >
  Executes the Universal Autonomous Time-Locked Self-Healing QA Loop across Web (CDP) and Mobile (ADB)
  applications. Enforces the 4 Ironclad Locks (Hardware Deadline Gate, Disk State Ledger, Git Ratchet
  Rollback, and Watchdog Timer) across a 7-Tier Rotating Verification Matrix.
license: Apache-2.0
---

# Universal Git-Ratcheted Autonomous Self-Healing Loop

## 1. The 4 Ironclad Locks (Zero-Regression Guarantees)

1. **Lock 1 — Hardware Deadline Gate:** Computes deterministic `START_EPOCH` and `DEADLINE_EPOCH` timestamps before execution begins.
2. **Lock 2 — Disk State Ledger (`AUTONOMOUS_LOOP_LEDGER.md`):** Persists pass-by-pass telemetry, defects discovered, root causes resolved, and remaining variance to disk so state survives context window compaction.
3. **Lock 3 — Deterministic Git Ratchet:**
   - Creates a **Cycle 0 Pre-Loop Baseline Commit** before any autonomous edit.
   - After every green verification tier (`exit_code == 0` and zero DOM/AST regressions), creates an atomic checkpoint commit.
   - If any autonomous modification introduces a build, test, or layout regression, immediately executes `git checkout -- .` back to the last verified green ratchet commit while preserving the ledger.
4. **Lock 4 — Asynchronous Watchdog:** Schedules non-blocking wakeup checks until the full time budget completes.

## 2. The 7-Tier Rotating Engineering Matrix

- **Tier 1:** Core Architecture, AST Import Boundaries & Zero Swallowed Exceptions
- **Tier 2:** Live Route Crawl, Console Error Zero & 4xx/5xx Network Telemetry
- **Tier 3:** 3-Pass Multi-Source Data Reconciliation & Boundary Pagination
- **Tier 4:** Concurrency Race Conditions, Request Debouncing & Heap Memory Leak Probes
- **Tier 5:** Dirty Data Injection, Malformed Payloads & Form Boundary Fuzzing (XSS/SQLi/Overflow)
- **Tier 6:** Mathematical CSS/UI Bounds (`scrollWidth <= clientWidth`), Tap Targets ($\ge 44\text{px}$), and Core Web Vitals (LCP, CLS, TTFB)
- **Tier 7:** High-Craft UI/UX Design Token Alignment & Tabular Telemetry Polish
