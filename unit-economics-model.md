# Unit Economics Framework

> A working model for evaluating growth channel health across CAC, LTV, contribution margin, and ROAS. Built from experience across fintech, payments, and consumer products.

---

## Why unit economics before roadmap

Every feature has a cost and a return. Before prioritising a growth initiative, I run it through this model to answer three questions:

1. What does it cost to acquire a user through this channel?
2. What is that user worth over their lifetime?
3. Is the margin after variable costs positive — and by how much?

Without this, roadmap prioritisation is just opinion.

---

## 1. Customer Acquisition Cost (CAC)

```
CAC = Total acquisition spend (channel) / New customers acquired

Blended CAC = Total marketing + sales spend / Total new customers
```

### What to watch

| Signal | Interpretation |
|---|---|
| CAC rising MoM | Channel saturating or bid competition increasing |
| CAC > LTV | Unsustainable — fix before scaling spend |
| Blended CAC < channel CAC | Organic / referral is subsidising paid — protect it |
| CAC payback > 12 months | High risk for subscription or lending products |

### CAC by channel (template)

| Channel | Spend | New Users | CAC | CAC Payback |
|---|---|---|---|---|
| Paid search | ₹X | X | ₹X | X months |
| Paid social | ₹X | X | ₹X | X months |
| Referral | ₹X | X | ₹X | X months |
| Organic / SEO | ₹0 | X | ₹0 | — |
| **Blended** | **₹X** | **X** | **₹X** | **X months** |

---

## 2. Lifetime Value (LTV)

```
LTV = ARPU × Gross Margin % × Average Customer Lifetime

where:
  ARPU = Average Revenue Per User (monthly or annual)
  Gross Margin % = (Revenue - COGS) / Revenue
  Average Customer Lifetime = 1 / Monthly Churn Rate
```

### LTV variants

| Variant | Formula | Use case |
|---|---|---|
| Simple LTV | ARPU × lifetime | Quick sanity check |
| Discounted LTV | Σ (monthly margin / (1+r)^t) | More accurate for long-lifecycle products |
| Predicted LTV (pLTV) | ML model on cohort behaviour | Paid UA bidding, high-volume consumer |

### LTV:CAC ratio benchmarks

| Ratio | Signal |
|---|---|
| < 1:1 | Destroying value — stop scaling |
| 1:1 – 2:1 | Breaking even — optimise before scaling |
| 3:1 | Healthy — standard benchmark for SaaS / fintech |
| > 5:1 | Strong — consider increasing spend to capture market |

---

## 3. Contribution Margin

### CM1 — After variable costs

```
CM1 = Revenue − Cost of Goods Sold (COGS) − Variable Fulfilment Costs

Examples of variable costs in fintech:
  - Payment gateway fees
  - KYC / bureau pull costs
  - SMS / WhatsApp notification costs
  - Loan disbursement charges
```

### CM2 — After marketing spend

```
CM2 = CM1 − Performance Marketing Spend

This is the most honest view of channel profitability.
A channel with positive CM1 but negative CM2 is not yet profitable.
```

### CM layer model (template)

| Line item | Per user (₹) | % of Revenue |
|---|---|---|
| Revenue | X | 100% |
| − Payment processing | X | X% |
| − KYC / bureau cost | X | X% |
| − Ops / servicing cost | X | X% |
| **= CM1** | **X** | **X%** |
| − Paid acquisition (CAC) | X | X% |
| **= CM2** | **X** | **X%** |
| − Fixed overhead allocation | X | X% |
| **= CM3 / Contribution** | **X** | **X%** |

---

## 4. ROAS (Return on Ad Spend)

```
ROAS = Revenue attributed to ad spend / Ad spend

Example: ₹4,00,000 revenue from ₹1,00,000 spend = 4x ROAS
```

### ROAS vs ROI — when to use which

| Metric | Use when |
|---|---|
| ROAS | Evaluating a specific paid channel or campaign |
| ROI / CM2 | Evaluating overall business profitability of a growth initiative |

ROAS alone is misleading — a 5x ROAS on a low-margin product may still be CM2-negative.

### Minimum viable ROAS

```
Break-even ROAS = 1 / Gross Margin %

Example: 40% gross margin → break-even ROAS = 2.5x
Anything below 2.5x is losing money at CM1 level.
```

---

## 5. Cohort analysis template

Track these by acquisition month to catch early churn signals:

| Cohort (month) | M0 | M1 | M2 | M3 | M6 | M12 |
|---|---|---|---|---|---|---|
| Users acquired | X | | | | | |
| Retained | 100% | X% | X% | X% | X% | X% |
| Revenue (cumulative) | ₹X | ₹X | ₹X | ₹X | ₹X | ₹X |
| Cumulative CAC recovered | 0% | X% | X% | X% | X% | X% |

**What to look for:** The month where cumulative revenue crosses CAC is your payback period. If it never crosses within 12 months for a monthly-subscription product, the unit economics don't work at current CAC.

---

## 6. PM decision rules

| Situation | Action |
|---|---|
| CAC payback > 18 months | Do not scale spend — fix retention or ARPU first |
| CM2 negative but CM1 positive | Marketing is the problem — cut spend or change channel |
| LTV:CAC < 2:1 | Freeze new channel experiments — fix the core loop |
| ROAS > break-even but CM2 negative | High COGS — product margin problem, not marketing problem |
| Cohort M3 retention < 40% | Activation / onboarding problem — product fix before growth |

---

## References & further reading

- [Andreessen Horowitz — Unit Economics](https://a16z.com/2015/08/21/16-metrics/)
- [Lenny Rachitsky — What is good retention](https://www.lennysnewsletter.com/p/what-is-good-retention-benchmarks)
- [David Sacks — The SaaS Adventure](https://www.youtube.com/watch?v=7r0LvBNf3J0)
