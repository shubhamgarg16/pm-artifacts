# PRD: [Feature / Product Name]

> **Status:** Draft / In Review / Approved  
> **Author:** Shubham Garg  
> **Last updated:** YYYY-MM-DD  
> **Stakeholders:** [Engineering Lead, Design, Growth, Compliance, Finance]  
> **Target release:** [Quarter / Sprint]

---

## 1. Problem statement

_One paragraph. What is broken, missing, or suboptimal? Who feels the pain? What is the measurable cost of inaction?_

**Example:**
> Borrowers who complete loan applications drop off at 34% during the document upload step. This costs us ~$280K in monthly funded loan revenue and increases servicer manual intervention by 60%.

---

## 2. Goal

| Type | Metric | Current | Target | Timeline |
|---|---|---|---|---|
| Primary | [e.g. Drop-off rate at doc upload] | [X%] | [Y%] | [Q] |
| Secondary | [e.g. Manual ops tickets] | [X/week] | [Y/week] | [Q] |
| Guardrail | [e.g. Compliance breach rate] | [X%] | ≤ [X%] | Ongoing |

**In scope:** _What this PRD covers._  
**Out of scope:** _What it explicitly does not cover (reduces scope creep)._

---

## 3. User personas

### Primary user
- **Who:** [Role / segment]
- **Context:** [When do they encounter this?]
- **Pain:** [What frustrates them today?]
- **Win:** [What does success feel like for them?]

### Secondary user
- **Who:** [e.g. Ops agent, compliance reviewer, partner bank]
- **Context / Pain / Win:** [Same format]

---

## 4. User stories

```
As a [persona],
I want to [action],
So that [outcome].

Acceptance criteria:
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
```

_Add one block per major user story. Aim for 3–6 stories per PRD._

---

## 5. Solution overview

_Describe the solution in plain language first. No wireframes yet. What changes for the user?_

### Option A — [Recommended]
- Description
- Pros
- Cons
- Estimated effort: [S / M / L / XL]

### Option B
- Description
- Pros
- Cons
- Estimated effort: [S / M / L / XL]

**Decision:** Option A, because [one-line rationale tied to goal metrics].

---

## 6. Functional requirements

| # | Requirement | Priority | Notes |
|---|---|---|---|
| F1 | [What the system must do] | Must-have | |
| F2 | [What the system must do] | Must-have | |
| F3 | [What the system should do] | Should-have | |
| F4 | [What the system could do] | Nice-to-have | |

_Use MoSCoW (Must / Should / Could / Won't). Be ruthless with Must-haves — if everything is critical, nothing is._

---

## 7. Non-functional requirements

| Requirement | Spec |
|---|---|
| Latency | API response < 300ms at p95 |
| Uptime | 99.9% SLA |
| Security | PCI-DSS / RBI / [relevant standard] compliant |
| Scalability | Handle [X] concurrent users / [Y] TPS |
| Auditability | All state changes logged with user ID + timestamp |

---

## 8. Dependencies & risks

| Item | Type | Owner | Mitigation |
|---|---|---|---|
| [e.g. KYC API v2 contract] | Dependency | [Team] | Confirm by [date] |
| [e.g. Regulatory approval delay] | Risk | Compliance | Build feature-flagged; ship to internal only first |
| [e.g. Third-party SDK upgrade] | Risk | Engineering | Parallel test environment |

---

## 9. Compliance & regulatory notes

_Fintech-specific section. Call out any RBI, SEBI, PCI-DSS, GDPR, or partner bank requirements that affect the feature. Never leave this blank._

- [ ] Legal review required: Yes / No
- [ ] Data residency constraints: [Yes — India only / No]
- [ ] Audit trail required: Yes / No
- [ ] Partner / bank approval gate: Yes / No

---

## 10. Metrics & instrumentation

**How will we know it worked?**

| Event | Tool | Owner |
|---|---|---|
| [e.g. doc_upload_started] | Mixpanel / Amplitude | PM |
| [e.g. doc_upload_completed] | Mixpanel / Amplitude | PM |
| [e.g. manual_review_triggered] | Internal dashboard | Ops |

**Review cadence:** Week 1 daily, Week 2–4 weekly, Month 2+ monthly.

---

## 11. Open questions

| # | Question | Owner | Due |
|---|---|---|---|
| Q1 | [Unresolved design or technical question] | [Name] | [Date] |
| Q2 | | | |

---

## 12. Appendix

- Wireframes / Figma link: [URL]
- Related PRDs: [Links]
- Data / research: [Links]
- Slack thread: [Link]
