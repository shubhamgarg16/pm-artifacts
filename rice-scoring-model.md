# RICE Prioritization Model

> A fintech-tuned RICE scoring framework for feature and initiative prioritization. Designed for growth-oriented product teams working across lending, payments, and platform products.

---

## The RICE formula

```
RICE Score = (Reach × Impact × Confidence) / Effort
```

| Factor | Definition | Scale |
|---|---|---|
| **Reach** | How many users affected per quarter | Absolute number |
| **Impact** | How much it moves the primary metric | 0.25 / 0.5 / 1 / 2 / 3 |
| **Confidence** | How sure are we about R, I, and E | 50% / 80% / 100% |
| **Effort** | Person-months of total team effort | Absolute number |

---

## Impact scale — fintech calibration

| Score | What it means | Example |
|---|---|---|
| 3 | Massive — moves a north star metric | Reduce doc drop-off by 15% → +₹50L/month funded |
| 2 | High — meaningful metric movement | Add NACH auto-debit → reduce manual collections by 30% |
| 1 | Medium — noticeable improvement | Improve repayment reminder UX → +5% on-time rate |
| 0.5 | Low — minor improvement | Better error messages on KYC failure |
| 0.25 | Minimal — cosmetic or edge case | Update FAQ page |

---

## Confidence guide

| % | Use when |
|---|---|
| 100% | A/B tested, validated with data, seen this pattern before |
| 80% | Strong qualitative signal, some data, reasonable analogy |
| 50% | Gut feel, new territory, limited data |

_Never use 100% confidence for a new channel or user segment you haven't shipped to before._

---

## Scoring template

| # | Initiative | Reach | Impact | Confidence | Effort | RICE Score | Notes |
|---|---|---|---|---|---|---|---|
| 1 | [Feature name] | X users | X | X% | X months | **X** | |
| 2 | [Feature name] | X users | X | X% | X months | **X** | |
| 3 | [Feature name] | X users | X | X% | X months | **X** | |

**Sort by RICE Score descending. Ship in that order unless a strategic override applies.**

---

## Strategic overrides — when to deviate from RICE

RICE is a tool, not a mandate. Override it (and document why) in these situations:

| Situation | Override action |
|---|---|
| Regulatory / compliance requirement | Bump to top regardless of score |
| Contract commitment to a major client | Treat as P0 with hard deadline |
| Dependency blocker for a high-RICE item | Ship the blocker first |
| Existential retention risk | Treat as immediate — RICE doesn't capture urgency well |
| Strategic bet (new market, new segment) | Accept lower score; set a learning goal instead of a metric goal |

---

## A worked example — MPOWER-style

**Initiative:** Add WhatsApp-based document upload for borrowers (instead of portal-only)

| Factor | Value | Reasoning |
|---|---|---|
| Reach | 4,200 users/quarter | All new borrowers in doc upload stage |
| Impact | 2 | Drops doc upload time from 3 days to same-day — direct LTV impact |
| Confidence | 80% | Validated by ops team data; similar feature worked at competitor |
| Effort | 1.5 person-months | Engineering estimate confirmed |

```
RICE = (4,200 × 2 × 0.80) / 1.5 = 4,480
```

This scored higher than a dashboard redesign (RICE: 820) and a new repayment channel (RICE: 2,100) — so it shipped first.

---

## Anti-patterns to avoid

- **HiPPO override** — "The CEO wants this" is not a RICE input. Translate the request into user reach and impact, then score it.
- **Effort underestimation** — Engineers give optimistic estimates. Add 30% buffer for integrations with third-party APIs (especially in fintech).
- **Ignoring dependencies** — A feature with RICE 9,000 that's blocked on a vendor contract for 6 months is effectively RICE 0 this quarter.
- **Scoring everything at 80% confidence** — If you're defaulting to 80%, you're not thinking hard enough about what you actually know.
