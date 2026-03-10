# Target Scoring Playbook — Framework v2

**Dutchess Management | Confidential**

This playbook documents the scoring methodology for acquisition targets using Framework v2 ("The Moat in the Machine"). Vertical-level scoring uses the Napkin (Q1/Q2/Q3, weighted 60/60/40) and quadrant classification. Company-level scoring uses Wind/Sail/Fit/AI Signal (N=171 backtest).

---

## 1. Quadrant Classification

Boundaries: A_v >= 40% task automatability = high automation; D_v >= 0.70 Defensibility Index = high defensibility.

| Quadrant | Definition | Margin Retention | Target MOIC |
|---|---|---|---|
| AI Goldmine | High auto, high moat — deploy AI, moat protects margin | 80-90% | ~2.1x |
| Contrarian Bet | Low auto, high moat — safe harbor + Physical AI optionality | 85-95% | 1.9-2.3x |
| Sand Castle | High auto, low moat — AI value flows to competitors/clients | 25-40% | ~0.48x (avoid) |
| Rising Tide | Low auto, low moat — consolidation play, not an AI play | 50-65% | Varies |

**Key interaction effect:** Defensibility predicts valuations only when automation is high. Among high-auto verticals, licensing ~ rank order of multiples (omega = +0.826, p = 0.011). Among low-auto verticals, no predictive power (omega = +0.132, p = 0.756).

---

## 2. Vertical-Level Scoring: The Napkin

Score the target's vertical using three questions (1-5 Likert, weighted 60/60/40):

| Question | Weight | What It Measures |
|---|---|---|
| Q1: Can AI do the work? | 60 | GenAI task automatability % of core revenue-generating work |
| Q2: Can you keep the gains? | 60 | Defensibility Index (Eq. 1 below) |
| Q3: Can a robot show up? | 40 | Physical AI / TSR margin lift |

**Defensibility Index (equal-weighted):**

D_v = (L_v + (1 - C_v / C_max) + P_v) / 3

- L_v = licensing proportion (BLS)
- C_v = annual churn; C_max = 0.35 (Staffing) for core 16
- P_v = physical presence proportion (BLS)

**Composite Score** S_v = 0.6 * Q1 + 0.6 * Q2 + 0.4 * Q3

---

## 3. Company-Level Scoring: Wind / Sail / Fit / AI Signal

### 3.1 Wind (Vertical Composite)

Wind = the vertical's composite score S_v assigned to each company.

- Backtest: r = +0.201, p = 0.008 — **only significant predictor of returns**

### 3.2 Sail (Company AI Readiness)

Sail = normalized(R&D intensity + AI patent count + management AI commentary)

- Backtest: r = +0.055, p = 0.478 — NOT statistically significant

### 3.3 Fit (Valuation Attractiveness)

Fit = normalized(inverse EV/Revenue, adjusted for growth)

- Backtest: r = -0.343, p = 0.000 — significant but reflects size proxy

### 3.4 AI Signal

AI Signal = normalized(R&D intensity x AI keyword frequency in 10-K filings)

- Backtest: r = -0.202, p = 0.008 — significant but **negative** (hype discount)

### 3.5 Interpretation

1. **Vertical selection dominates.** Wind is the only subscore that reliably predicts returns.
2. **Valuation discipline matters but confounded.** Fit proxies for firm size.
3. **Company AI readiness is noise.** Don't overpay for "AI-ready" companies.
4. **AI hype is a negative signal.** High AI Signal correlates with worse returns.

---

## 4. Investment Logic by Quadrant

### AI Goldmine (High auto, high moat)
- **Thesis:** Deploy AI to automate high-automatability tasks; moat protects margin retention at 80-90%.
- **Playbook:** Acquire, invest in AI tooling, harvest margin expansion behind defensive moat.

### Contrarian Bet (Low auto, high moat)
- **Thesis:** Safe harbor from GenAI disruption. Physical AI provides optionality.
- **Playbook:** Acquire for cash flow stability + Physical AI optionality.

### Sand Castle (High auto, low moat)
- **Thesis:** Default: Avoid. AI value flows to clients/competitors. Margin retention 25-40%.
- **Playbook:** Do not acquire UNLESS all four conditions met:
  1. Identifiable pivot asset (regulatory, proprietary data, >500 enterprise logos, domain IP)
  2. Entry valuation 2-4x revenue with 30-50% earnout
  3. Credible pivot path <24 months
  4. Downside protection (positive cash flow, >80% GRR, 1-2x terminal without pivot)

### Rising Tide (Low auto, low moat)
- **Thesis:** Consolidation play, not an AI play.
- **Playbook:** Standard PE roll-up economics.

---

## 5. Software Target Overlay

### 5.1 Switching Cost Depth (SC_Depth)

Five-factor weighted rubric (each scored 1-5):

| Dimension | Weight | What It Captures |
|---|---|---|
| Workflow & Compliance Embedding | 30% | System-of-record, process dependency, regulatory re-cert, compliance certs |
| Data Gravity & Format Lock-In | 25% | Data volume, proprietary schema, retention requirements |
| Technical Integration Complexity | 20% | Integration count, API dependencies, SI ecosystem |
| Financial & Contractual Lock-In | 15% | Contract length, ETFs, implementation amortization |
| Relationship & Brand Ownership | 10% | Direct end-user relationship, brand equity, NPS, CS depth |

SC_Depth = 0.30 x D1 + 0.25 x D2 + 0.20 x D3 + 0.15 x D4 + 0.10 x D5

For Defensibility Index: SC_Depth_normalized = (SC_Depth - 1) / 4 replaces (1 - C_v/C_max).

### 5.2 Data Moat Classification

Apply Travis May's six-type taxonomy. Test: (1) substantial competitive value? (2) genuinely prevents competitor access? (3) no functional substitutes incl. synthetic data?

### 5.3 Platform/Ecosystem Moat

Score across: ecosystem depth, integration moat depth, network effect strength, switching cost friction, ecosystem governance. NRR >120% is the single best proxy.

### 5.4 Composite Software Moat Score

Software_Moat = 0.30 x SC_Depth + 0.25 x DataNet + 0.20 x Expansion + 0.15 x Displacement + 0.10 x AI_Trajectory

| Score | Tier | CAP | PE Implication |
|---|---|---|---|
| 4.5-5.0 | Wide Moat | 15+ yr | Premium valuation. Underwrite price increases. |
| 3.5-4.4 | Narrow Moat | 7-15 yr | Standard PE. Moat deepening is the thesis. |
| 2.5-3.4 | Nascent Moat | 3-7 yr | Discount for moat risk. Execution-dependent. |
| <2.5 | No Moat | <3 yr | Avoid as platform investment. Growth story only. |

---

## 6. Partnership Dependency Scoring

Applied when a single partnership contributes >15% of revenue. Risk score 1-5 (inverted — 5 = highest risk):

| Score | Revenue Dependency | Exclusivity | Termination Risk | Integration Depth |
|---|---|---|---|---|
| 5 | >50% of revenue | Exclusive | At will, <90 days | Shallow (API only) |
| 4 | 30-50% | Preferred | 6-12 month terms | Moderate |
| 3 | 15-30% | Non-exclusive | 1-2 year terms | Deep |
| 2 | 5-15% | Non-exclusive | 2+ year terms | Deep, mutual |
| 1 | <5% | Diversified | Long-term, strategic | Platform-level |

Score >= 4: flag as gating diligence item.

---

## 7. Pricing Model Vulnerability

Score 1-5 (5 = most durable):

| Score | Model | AI Resilience |
|---|---|---|
| 5 | Outcome/value-based or regulatory-mandated | Highest |
| 4 | Platform subscription + consumption upside | High |
| 3 | Hybrid (seat + consumption) | Medium |
| 2 | Pure per-seat/per-agent | Low |
| 1 | Per-minute/per-interaction in AI-automatable domain | Lowest |

If score <= 2: cap AI_Trajectory at 3 in Software_Moat composite. Require pricing pivot scenario in 100-Day Phase 5.

---

## 8. V2 Rescore Triggers

- Data delta >15% from v1
- Composite score within 5 points of quadrant boundary
- Material new information
- IC request
- Partner concentration >30% discovered during diligence

V2 refinements: name specific competitors, target data gaps, include vertical-specific AI threats, request pricing model data, cross-validate bull vs bear.
