---
name: cdp-web-telemetry-suite
description: >
  High-speed Chrome DevTools Protocol (CDP) single-pass telemetry suite for web applications.
  Extracts WCAG 2.2 AA/AAA contrast ratios, Core Web Vitals (LCP, CLS, TTFB), JS Heap memory snapshots,
  JSON-LD Schema.org validity, and visual layout regressions (overlapping DOMrects & clipped text) in a single batched execution.
license: Apache-2.0
---

# Batched CDP Web Telemetry & Visual Regression Suite

## Capabilities
1. **WCAG 2.2 AA/AAA Contrast & Tap-Target Auditor:** Computes relative luminance across foreground/background computed styles, flags tap targets $< 44\times 44\text{px}$, and verifies ARIA landmark focus traps.
2. **Visual Layout & Bounding-Box Diff Engine:** Scans all visible DOM nodes via `getBoundingClientRect()` to detect sibling collisions, horizontal viewport overflow (`document.documentElement.scrollWidth > window.innerWidth`), and text truncation (`scrollWidth > clientWidth`).
3. **Core Web Vitals & JS Heap Probe:** Extracts Navigation Timing API metrics (`TTFB`, `FCP`, `LCP`, `CLS`) and `performance.memory.usedJSHeapSize` to catch memory leaks across route transitions.
