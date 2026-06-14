# Now / Next / Later Roadmap

> A horizon-based roadmap structure for fintech and platform products. Designed to communicate direction without over-committing to dates — especially useful when working across engineering, growth, compliance, and leadership stakeholders.

---

## Why Now / Next / Later over a Gantt

| Gantt / date-based | Now / Next / Later |
|---|---|
| Implies false precision | Communicates direction, not dates |
| Gets stale immediately | Stays relevant for an entire quarter |
| Invites negotiation on timelines | Invites conversation on priorities |
| Breaks trust when dates slip | Builds trust by being honest about uncertainty |

_Use Gantt for sprint-level execution. Use Now/Next/Later for stakeholder alignment and strategic planning._

---

## Horizon definitions

| Horizon | Timeframe | State of confidence |
|---|---|---|
| **Now** | Current sprint / month | Fully scoped, in development or ready to build |
| **Next** | Next 1–2 quarters | Problem validated, solution being designed |
| **Later** | Beyond that | Strategic direction, not yet scoped |

---

## Template

### North star metric
_The single metric this roadmap is optimising for this half._

> Example: Reduce time-to-disbursement from 5 days to 2 days for 80% of borrowers by Q3.

---

### Now — In flight

| Initiative | Goal | Owner | Status |
|---|---|---|---|
| [Feature / project name] | [What metric it moves] | [Team / person] | In dev / In review / Shipped |
| | | | |

---

### Next — Coming up

| Initiative | Why it matters | Dependencies | Confidence |
|---|---|---|---|
| [Feature / project name] | [Impact on north star] | [Blocker or dependency] | High / Medium / Low |
| | | | |

---

### Later — On the horizon

| Initiative | Hypothesis | Open questions |
|---|---|---|
| [Feature / project name] | [What we believe and why] | [What we need to learn first] |
| | | |

---

### Not doing (and why)

_Equally important. Listing what's off the roadmap prevents stakeholders from re-raising the same ideas every sprint._

| Initiative | Reason not prioritised |
|---|---|
| [Feature] | Low RICE score — revisit next half |
| [Feature] | Blocked on regulatory approval |
| [Feature] | Deprioritised in favour of [higher-impact initiative] |

---

## A worked example — VeeFly AI Suite

### North star metric
> Increase creator-activated users (users who publish at least one AI-generated piece of content) from 12% to 35% by end of Q3.

---

### Now

| Initiative | Goal | Owner | Status |
|---|---|---|---|
| AI caption generator (v1) | Reduce time-to-first-post for new creators | Product + Eng | In dev |
| Onboarding flow redesign | Lift D7 activation from 18% to 30% | Product + Design | In review |

---

### Next

| Initiative | Why it matters | Dependencies | Confidence |
|---|---|---|---|
| AI thumbnail generator | Top creator request; direct impact on CTR | Design asset pipeline | High |
| Niche content calendar | Reduces creator churn at D30 | NLP model fine-tuning | Medium |
| Brand kit integration | Unlocks B2B creator segment | API partner scoping | Low |

---

### Later

| Initiative | Hypothesis | Open questions |
|---|---|---|
| AI video script generator | Video creators are highest-LTV segment | Do we have enough training data? What's the infra cost? |
| Creator analytics dashboard | Better insights → higher retention | Which metrics actually change creator behaviour? |

---

### Not doing this quarter

| Initiative | Reason |
|---|---|
| Multi-language content support | Requires significant NLP investment; lower RICE than core activation |
| Marketplace for creator templates | Premature — need more creators on platform first |

---

## How to present this to stakeholders

**To engineering:** Share the Now column in detail. Discuss Next to get early scoping input. Keep Later loose.

**To leadership:** Lead with the north star metric and the Now/Next horizon. Use Later to show you're thinking ahead without creating false commitments.

**To growth / marketing:** Focus on the activation and retention initiatives. Tie each to the unit economics impact (LTV, CAC payback).

**Cadence:** Review Now weekly in sprint. Review full roadmap monthly with stakeholders. Re-score Later items quarterly.
