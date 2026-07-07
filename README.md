# DTC Retention & CAC Payback Analysis
**Author:** Kathy Presto | [LinkedIn](https://linkedin.com/in/k-presto) | 
[GitHub](https://github.com/Katpresto123)

## Overview
This project demonstrates cohort retention analysis and CAC payback modeling 
applied to e-commerce transaction data — a framework any DTC brand can replicate 
on their own data.

The analysis answers one question most DTC brands can't: **is your retention rate 
high enough to justify what you're spending to acquire customers?**

## The Business Problem
Customer acquisition costs have risen 222% over the past eight years. The average 
DTC brand retains just 28.2% of customers. Yet most brands keep pouring budget into 
acquisition without knowing their break-even retention rate.

This analysis makes that number concrete — by category, by month, by retention 
scenario.

## Dataset
**UCI Online Retail Dataset** — 541,909 real transactions from a UK-based online 
retailer (Dec 2010 – Dec 2011).

This dataset is used as a vehicle to demonstrate cohort methodology. The framework 
is designed to be replicated with any transactional dataset containing customer IDs, 
order dates, and revenue. Current DTC CAC benchmarks (2025-2026) are layered in to 
ground the analysis in today's reality.

## What's In This Notebook
1. **Data cleaning** — handling cancellations, missing IDs, outlier removal
2. **Cohort retention matrix** — 13 monthly cohorts tracked over 12 months
3. **Retention heatmap** — visual cohort performance over time
4. **Revenue heatmap** — average revenue per returning customer by cohort
5. **Month-1 retention vs industry benchmark** — how each cohort stacks up 
   against the 28.2% industry average
6. **CAC break-even model** — months to payback across 4 DTC categories at 
   6 retention scenarios
7. **DTC Playbook** — actionable tactics by category based on the analysis

## Key Findings
- Only 1 of 12 cohorts beat the industry average retention rate of 28.2%
- Month-1 retention ranged from 11% to 37% — a 3x spread driven by acquisition 
  quality, not just retention tactics
- At 28.2% industry average retention, supplement brands never recover CAC 
  within 12 months
- Food brands need 25%+ retention just to break even in a year

## CAC Benchmarks Used (2025-2026)
| Category | CAC (USD) | CAC (GBP) |
|----------|-----------|-----------|
| Pet | $23 | £18.17 |
| Beauty | $42 | £33.18 |
| Food | $51 | £40.29 |
| Supplements | $89 | £70.31 |

*Source: First Page Sage, based on $47M in managed DTC ad spend*


## Playbook - What to do about it by category

**🐾 Pet (CAC: ~£18 | Breaks even at 15% retention by month 8)**
Low CAC means you can acquire aggressively. Focus energy on months 2-3 — 
get a second purchase fast and the payback math works in your favor.
- Post-purchase email sequence with complementary products
- Subscription nudge at reorder window (food/treats especially)
- Loyalty points from first purchase

**💄 Beauty (CAC: ~£33 | Needs 20%+ retention to break even in 12 months)**
You're one bad acquisition month away from CAC that never pays back.
- First 30 days are critical — onboarding sequence, how-to content, replenishment reminders
- Bundle first purchase to increase AOV and compress payback timeline
- Earned loyalty tier after second purchase to lock in behavior

**🍔 Food (CAC: ~£40 | Needs 25%+ retention to break even in 12 months)**
Subscription is your best friend. One-time buyers are expensive.
- Default to subscription at checkout with easy pause/cancel (reduces friction objection)
- Reorder reminder before they run out — timing is everything in consumables
- Win-back sequence at day 45 if no second purchase

**💊 Supplements (CAC: ~£70 | Needs 40% retention just to break even in 12 months)**
The math is brutal without a subscription model. At industry average retention of 28.2% 
you are losing money on every customer for the entire first year.
- Subscription-first business model — one-time purchase pricing should be meaningfully 
  higher to reflect true acquisition cost
- 90-day supply bundles to extend reorder window and improve margins
- Results-based content to justify continued purchase (before/after, education)
- At-risk trigger at day 60 with a personal outreach or survey

## Tech Stack
- Python 3.12
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

## How to Run
1. Download the UCI Online Retail dataset (.xlsx) from 
   [UCI ML Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
2. Place `Online Retail.xlsx` in the same directory as the notebook
3. Run all cells in order

## Replicate This With Your Own Data
Any transactional dataset with these three fields works:
- Customer ID
- Order date
- Order value

The cohort logic and CAC model are fully portable.
