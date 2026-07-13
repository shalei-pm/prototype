# Payment Flow Prototypes Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Extend prototype 04 with payment confirmation, QR payment, success, and incomplete-payment states, then show the purchased project selected in prototype 05.

**Architecture:** Keep all payment screens in the existing `project-confirm-flow-draft.html` unit stack so the integrated review page can embed each state independently. Reuse the current Pad shell, top bar, bottom action bar, typography, and square-corner button system; add one local non-payment QR bitmap asset for the scan state.

**Tech Stack:** Static HTML, CSS, local PNG asset, iframe-based integrated review page.

---

### Task 1: Add Payment State UI

**Files:**
- Create: `prototype/assets/payment-qr-demo.png`
- Modify: `prototype/drafts/project-confirm-flow-draft.html`

- [x] Generate a local QR bitmap containing non-payment demo text.
- [x] Add shared payment overlay, payment page, result page, pricing summary, countdown, and provider-mark styles.
- [x] Add `04-A` confirmation overlay, `04-B` 60-second QR payment, `04-C` success, and `04-D` incomplete-payment units after prototype 04.
- [x] Update prototype 05 so the newly purchased project is first, marked as just purchased, and selected for today's treatment.

### Task 2: Update Review Index And Documentation

**Files:**
- Modify: `prototype/integrated-review-current.html`
- Modify: `docs/design.md`
- Modify: `docs/codex-learning-state.md`

- [x] Add `04-A` through `04-D` to the left review index and prototype grid without renumbering `05-12`.
- [x] Update iframe unit indexes after inserting four payment units.
- [x] Record the 60-second payment window, success and failure destinations, and automatic asset selection rule.

### Task 3: Synchronize And Verify

**Files:**
- Modify: `.superpowers/brainstorm/54056-1783560685/content/prototypes/drafts/project-confirm-flow-draft.html`
- Modify: `.superpowers/brainstorm/54056-1783560685/content/prototypes/integrated-review-current.html`
- Create: `.superpowers/brainstorm/54056-1783560685/content/prototypes/assets/payment-qr-demo.png`

- [x] Synchronize public prototype sources to the hidden review copies.
- [x] Run `git diff --check`.
- [x] Verify all expected review IDs, iframe units, payment labels, and QR asset references with a deterministic source check.
- [x] Confirm public and hidden prototype copies are byte-identical.
