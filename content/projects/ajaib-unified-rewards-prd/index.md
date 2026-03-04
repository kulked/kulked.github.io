---
title: 'Ajaib Unified Rewards System (Genie) — PRD'
share: false
date: 2025-08-01
summary: >
  Product Requirements Document for Genie — Ajaib's unified rewards engine
  spanning stocks, crypto, mutual funds, payments, and savings. Covers
  reward types, campaign manager, AI/ML targeting, risk controls, and
  success metrics for Indonesia's fast-growing fintech market.
tags:
  - Product Discovery
links:
  - 
    icon_pack: fas
    name: View Detailed PDF
    url: /uploads/Ajaib_Unified_Rewards_System__PRD.pdf
---

<!-- ============================================================
  OPTION A — PDF IFRAME EMBED
  Use this body if you want to embed the PDF as-is.
  Delete Option B below if you choose this.
============================================================ -->

<!--<iframe
  src="/uploads/Ajaib_Unified_Rewards_System__PRD.pdf"
  width="100%"
  height="900px"
  style="border: none; border-radius: 8px; box-shadow: 0 4px 24px rgba(0,0,0,0.12);">
  <p>Your browser does not support iframes.
     <a href="/uploads/Ajaib_Unified_Rewards_System__PRD.pdf">Download the PDF</a>
  </p>
</iframe>-->

---

<!-- ============================================================
  OPTION B — ENHANCED MARKDOWN VERSION
  Delete Option A above and uncomment this block if you prefer it.
============================================================ -->



## Context: Indonesia's Fintech Landscape

Indonesia's fintech space is booming — ~280 million people, ~213 million internet users,
and digital adoption among the world's highest. **QRIS** (Bank Indonesia's payment standard)
had 54 million users and 35 million merchants as of Oct 2024, with e-money transactions
growing 27% YoY. Yet cash still dominates ~51% of POS value, leaving enormous headroom.

Ajaib's multi-product platform (stocks · crypto · mutual funds · bonds · QRIS payments ·
savings) is uniquely positioned to capture this opportunity through a **unified rewards engine**.

---

## Opportunity: Rewards as a Growth Lever

**Global Precedents:**
- **Robinhood:** Gamified referral offering free stocks — drove viral acquisition
- **SoFi:** Points system connecting banking, lending, and investing
- **Paytm:** Cashback/points spanning payments, investments, and commerce → 100M+ MAUs
- **PhonePe:** UPI rewards enabling ~50% market share in India

A unified rewards system for Ajaib can drive the same dynamics — sign-up incentives,
cross-product engagement, and long-term retention.

---

## Product Goals

> Increase user acquisition and activation · Boost transaction frequency and
> cross-product usage · Improve user LTV — while controlling reward cost and mitigating fraud.

---

## Reward Types

### 1. Acquisition Rewards
- **Cash/Stock Back (Referral):** Bonus for both referrer and new user on first trade
- **Welcome Bonus:** Cashback or deposit match for new users
- **Cross-Product Incentives:** Stock bonus for using payments, or free mutual fund for bill payments

### 2. Conversion Rewards
- **First Trade Reward:** Commission-free trade or bonus share
- **Gamified Incentives:** Milestone rewards ("10 trades this week — win a prize")
- **Behavioural Nudges:** Time-limited offers for specific actions

### 3. Loyalty Rewards
- **Loyalty Points:** 1 point per IDR 1,000 traded, redeemable for cash/assets/vouchers/airmiles
- **Bonus Interest:** Higher savings yield if balance or transaction criteria met
- **Tiered Subscription:** Premium benefits (enhanced support, waived fees) for loyalty-tier subscribers

### 4. Campaign Rewards
- **Merchant-Funded Deals:** 5% cashback on QRIS payments funded by merchants
- **Seasonal Promotions:** Holiday-themed campaigns

---

## Campaign Manager & Targeting

A **Central Campaign Manager** enables marketing/growth teams to configure and launch
reward campaigns with:

| Capability | Details |
|---|---|
| **Audience Targeting** | Demographics · Location · Device · Behavioural · Intent/Interest |
| **AI/ML Audiences** | Propensity-to-trade, predicted LTV, cross-product affinity segments |
| **Real-Time Audience Sizing** | Live reach estimates and audience overlap analysis |
| **Reward Capping** | Per-user caps, daily caps, and total budget caps |
| **Frequency Capping** | Limit reward triggers per day/week/month |
| **Real-Time Decisioning** | Campaign selection engine balancing relevance and revenue impact |
| **A/B Testing** | Framework for offer experimentation |
| **Dashboards** | Campaign ROI, fraud flags, and user engagement at a glance |

---

## Risk Prevention & Reward Disbursement

| Control | Detail |
|---|---|
| Eligibility Verification | KYC completed · One user per identity · No duplicate accounts |
| Abuse Detection | Flag multiple sign-ups from same device/IP · Repeated cancel-after-reward |
| Reward Audit Trails | Every disbursal logged; anomalies trigger alerts |
| Cost Controls | Soft and hard caps to ensure budget adherence |
| Staggered Payouts | High-value rewards released only after sustained activity (e.g. 7 days) |
| Compliance Checks | Cross-border crypto/securities rewards reviewed by legal |

---

## Success Metrics

| Priority | Metric | Target |
|---|---|---|
| P0 | Payback Period | Rewards Expenses / (Net New MRR × Gross Margin) |
| P0 | ROI | (Incremental revenue – reward cost) / reward cost |
| P0 | Cross-product adoption rate | Y% of users transacting on 2+ products |
| P0 | User Acquisition Cost | X% decrease |
| P0 | Customer Lifetime Value | Z% increase |

---

*Created By Kedarnath Kulkarni · Aug 2025 · IIM Ahmedabad MBA · Director of Product, Paytm*


