---
title: 'Declining KYC Pass Rate at Revolut — Analysis & Fixes'
date: 2025-03-01
summary: >
  Data-driven analytical breakdown of a declining KYC pass rate at Revolut.
  Diagnoses root causes by isolating document-check vs. face-similarity
  failures, breaks down issues by document type and nationality, and
  proposes targeted fixes with supporting evidence.
tags:
  - Analytical Reasoning
links:
  - 
    icon_pack: fas
    name: View Detailed PDF
    url: /uploads/Declining_KYC_Pass_Rate_at_Revolut__Analysis_and_Fixes.pdf
---

<!-- ============================================================
  OPTION A — PDF IFRAME EMBED
  Use this body if you want to embed the PDF as-is.
  Delete Option B below if you choose this.
============================================================ -->

<!--<iframe
  src="/uploads/Declining_KYC_Pass_Rate_at_Revolut__Analysis_and_Fixes.pdf"
  width="100%"
  height="900px"
  style="border: none; border-radius: 8px; box-shadow: 0 4px 24px rgba(0,0,0,0.12);">
  <p>Your browser does not support iframes.
     <a href="/uploads/Declining_KYC_Pass_Rate_at_Revolut__Analysis_and_Fixes.pdf">Download the PDF</a>
  </p>
</iframe>-->

---

<!-- ============================================================
  OPTION B — ENHANCED MARKDOWN VERSION
  Delete Option A above and uncomment this block if you prefer it.
============================================================ -->



## Problem Statement

Revolut's KYC (Know Your Customer) pass rate has been declining since July.
The KYC pipeline consists of two main checks:
1. **Document Check** — verifies the identity document (passport, driving licence, national ID)
2. **Face Similarity Check** — matches the user's selfie to the document photo

**Outcome Classification:**
- `1 = Clear` (pass)
- `0 = Consider` (fail / flagged for review)

---

## Visualising the Problem

Two key observations from the data:

> **Insight 1:** The "not clear" rate for the **face similarity check** has remained
> broadly stable month-over-month.

> **Insight 2:** The "not clear" rate for the **document check** has been climbing
> sharply since July — and is the primary driver of the declining overall pass rate.

**Conclusion:** The problem is localised to the **document check**, not face similarity.

---

## Symptoms — Document Check Failures

Two distinct failure patterns were identified within the document check:

| # | Symptom | Detail |
|---|---|---|
| **1** | Spike in "not clear" on the **Image Integrity test** | Cases failing image integrity despite clearing face similarity, data validation, visual authenticity, and showing no conclusive fraud evidence |
| **2** | Spike in **inconclusive outcomes** on visual authenticity, data validation, and fraud inspection | System unable to make a definitive pass/fail determination |

---

## Symptoms — Face Similarity Check Failures (Secondary)

| # | Symptom | Detail |
|---|---|---|
| **3** | Spike in "not clear" on **Face Image Integrity test** | Cases failing face image integrity despite clearing all document checks |
| **4** | Spike in **inconclusive face comparison outcomes** | Unable to determine pass/fail on face comparison despite clearing other sub-checks |

---

## Breaking Down by Document Type

Analysis of the "not clear" outcomes by document type (driving licence · national identity card · passport · NA) reveals which document categories are disproportionately contributing to failures — enabling targeted fixes.

---

## Breaking Down by Nationality

> **Insight:** The nationality data is sparsely populated in the dataset, making
> country-level analysis of limited utility. The primary breakdown should focus
> on document type and sub-check failure patterns.

---

## Root Cause Hypotheses

Based on the symptom analysis:

1. **Image quality degradation** — A change in the image capture or upload pathway (e.g. new app version, compression settings) may be causing previously-passing documents to fail image integrity checks.

2. **Algorithm or model change** — A threshold change in the document check model since July could be causing borderline cases to flip from "clear" to "consider."

3. **Document mix shift** — A change in the distribution of document types (more low-quality scans, new document formats) could be causing systemic failures on specific sub-checks.

---

## Proposed Fixes

| Fix | Target Symptom | Detail |
|---|---|---|
| Review image capture pipeline for quality regressions | Symptoms 1 & 3 | Audit any app or SDK changes deployed around July that could affect image resolution or compression |
| Audit document check model thresholds | Symptom 2 | Review whether any model update or threshold change coincided with the July spike |
| Implement fallback to manual review for inconclusive cases | Symptom 2 | Route "consider" cases with high confidence scores to a fast-track human review queue to protect pass rate while investigation is ongoing |
| Populate nationality field in the data pipeline | Symptom analysis | Fixing sparse nationality data would enable more targeted geographic/document-type analysis |

---

*Created By Kedarnath Kulkarni · IIM Ahmedabad MBA · Director of Product, Paytm*


