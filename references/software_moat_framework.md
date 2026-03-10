# Software Company Moat Framework — Research Synthesis

**Dutchess Management | Research Grounding**

This document synthesizes research on how to identify, measure, and score defensibility in software companies for PE/M&A investment decisions. It extends the Framework v2 Defensibility Index (which covers services verticals) into the software domain.

---

## 1. The Core Problem: Most Claimed Moats Are Illusory

The consensus from a16z, NFX, Morningstar, and Helmer's 7 Powers is stark: most software companies claiming moats — especially "data moats" and "platform moats" — do not have them. The distinction between real and illusory defensibility is the single most important diligence question for software acquisitions.

**Key finding from a16z ("The Empty Promise of Data Moats"):** Data value follows a diminishing curve. Beyond capturing ~40% of possible queries, additional data creates no measurable advantage. Most "data moats" are data *scale* effects (common, weak) not data *network* effects (rare, powerful).

**Key finding from NFX:** Network effects account for ~70% of value created in technology since 1994, but fewer than 15% of tech companies genuinely have them.

**Key finding from the N=171 backtest (Framework v2):** Wind (vertical selection) is the only subscore that significantly predicts returns. Company-specific factors (Sail, AI Signal) do not. This extends to software: *which category* you're in matters more than company-level execution claims.

---

## 2. Moat Taxonomy for Software Companies

### 2.1 Data Moats

**Travis May's Six Types (ordered by durability):**

| Type | Description | Example | Durability |
|---|---|---|---|
| Data Currency | Dataset all parties need to transact | FICO, DUNS, Nielsen, IQVIA benchmarks | Highest |
| Long-Tail Aggregation | Thousands of exclusive data partnerships | Bloomberg, Plaid, LexisNexis | High |
| Give-to-Get | Participants contribute to access aggregate | Credit bureaus, Glassdoor, Tegus | High |
| Exclusive Source | Early agreements with data originators | IQVIA pharmacy relationships | Medium |
| Proprietary Creation | Original data from panels/analysis/users | Gartner, Yelp, Nielsen panels | Medium |
| Exhaust Data | Secondary data from core operations | Amazon purchase data, Flatiron Health | Medium-High |

**The Three-Criteria Test (Abraham Thomas):** For data to be a moat it must simultaneously:
1. Offer **substantial** competitive value (not incremental)
2. **Genuinely prevent** competitors from accessing equivalent value
3. Have **no functional substitutes** (including synthetic data)

**The Flywheel Reality Check (NFX):** A data flywheel only compounds when ALL of:
- Data capture is automatic/passive
- Product improvement is continuous and perceptible to users
- Marginal data value doesn't asymptote quickly
- Data is central to core value (not peripheral)

**Freeze Test:** If you froze data collection today, how fast does your advantage erode?
- Immediately (real-time data like Waze) -> real flywheel
- 2-3 years (historical datasets) -> weak, not a moat
- Never (you have enough) -> you've hit the asymptote

**Real data moats:** Bloomberg Terminal, IQVIA, CoStar, credit bureaus, Tesla FSD
**Illusory data moats:** Netflix recommendations, meeting transcription apps, most vertical AI startups, Zillow (licensed data)

### 2.2 Platform & Ecosystem Moats

**Five Platform Types:**

| Type | Mechanism | Key Test | Example |
|---|---|---|---|
| Marketplace | Two-sided buyer/seller network | Is participation exclusive or multi-tenanted? | Upwork, eBay |
| Developer/API | Third-party code built on platform | What % of customer product depends on this API? | Twilio, Stripe |
| App Store/Extension | Third-party apps extend core product | Does marketplace generate customer acquisition? | Salesforce, Shopify |
| Integration Ecosystem | Connective tissue between enterprise systems | How many systems does it connect? | ServiceNow, Workday |
| Aggregator | Controls demand, commoditizes supply | Does it own the customer relationship? | Google, Veeva |

**Real Platform vs. Product Dressed Up:**

Green flags:
- 500+ active third-party integrations
- 15%+ of customer LTV tied to ecosystem
- 30%+ of new ARR partner-influenced
- NRR >120%
- Certified professional ecosystem (jobs depend on the platform)

Red flags:
- All integrations vendor-built
- Fewer than 50 marketplace apps
- Zero partner-sourced revenue
- Implementation takes <2 weeks (no workflow depth)
- NRR <110% despite "platform" positioning

**What breaks platform moats:** Not better products — paradigm shifts. The risk to ServiceNow/Salesforce isn't a better ITSM/CRM — it's AI-native delivery that bypasses the 12-month implementation entirely.

### 2.3 Switching Costs (Expanded from Framework v2)

**Dimension taxonomy:**

| Dimension | Weight | Durability | Primary Erosion Vector |
|---|---|---|---|
| Workflow & Compliance Embedding | 30% | HIGH | Would require AI to re-learn all embedded process logic |
| Data Gravity & Format Lock-In | 25% | MEDIUM (declining) | AI migration tools, EU Data Act, open standards |
| Technical Integration Complexity | 20% | MEDIUM | Open standards, iPaaS abstraction layers |
| Financial & Contractual Lock-In | 15% | LOW | Regulation (EU Data Act), customer leverage |
| Relationship & Brand Ownership | 10% | MEDIUM | Channel disintermediation, brand decay |

**Scoring Rubric (1-5 per dimension):**

**Workflow & Compliance Embedding (30%):**
- 5: System of record for regulated process. Multiple departments. Regulatory re-cert required to switch. Compliance certs (HIPAA BAA, FedRAMP, SOC 2 Type II) that customer compliance posture depends on.
- 4: Primary operational hub. Compliance configs embedded in vendor workflows.
- 3: Deeply used but not definitive system of record.
- 2: Accelerates workflows but doesn't define them. Replaceable in 3-6 months.
- 1: Productivity tool. Replace in 30-60 days.

**Data Gravity (25%):**
- 5: Multi-year longitudinal data, proprietary schema, regulatory retention (7+ yr), no clean export. >1TB/customer.
- 4: 3-5 years historical data, semi-proprietary format.
- 3: 1-3 years data. Export available but transformation needed.
- 2: Recent data (<1yr material), standard formats. AI-assisted migration viable.
- 1: Stateless. Data portability trivial.

**Technical Integration (20%):**
- 5: 10+ integrations with critical enterprise systems. SI firms have practices built around it.
- 4: 5-10 integrations with core systems. Third-party app ecosystem.
- 3: 3-5 integrations. Mix of native and custom.
- 2: 1-3 integrations via iPaaS. 1-3 months IT effort.
- 1: Zero integrations. Standalone tool.

**Financial/Contractual (15%):**
- 5: 3+ year contracts with material ETFs. >180-day notice.
- 4: 2-3 year contracts. Moderate ETFs.
- 3: Annual with auto-renewal. Implementation cost 1-3 months ARR.
- 2: Monthly/annual, no ETFs. 30-60 day exit.
- 1: Month-to-month/freemium. Zero friction.

**Relationship & Brand Ownership (10%):**
- 5: Direct end-user relationship. Category-defining brand. NPS >60. G2/Capterra >4.5 with >200 reviews.
- 4: Direct relationship for majority of revenue. Top-3 brand recall. NPS >40.
- 3: Mixed channel model. NPS 20-40. Reactive-to-proactive CS.
- 2: Primarily channel/reseller. Weak brand. Transactional CS.
- 1: No direct end-user relationship (white-label/OEM). No brand equity.

**Composite:**
```
SC_Depth = 0.30 * D1 + 0.25 * D2 + 0.20 * D3 + 0.15 * D4 + 0.10 * D5
```

| Score | Classification | GRR Expectation | Pricing Power |
|---|---|---|---|
| 4.0-5.0 | Deep Moat | >93% | Can raise 10-15% without churn |
| 3.0-3.9 | Moderate Moat | 88-93% | Some power, alternatives feasible |
| 2.0-2.9 | Shallow Moat | 80-88% | Limited, requires continuous product improvement |
| 1.0-1.9 | No Moat | <80% | None, prone to displacement |

---

## 3. Observable Metrics for Moat Assessment

| Metric | What It Signals | Benchmark (Best-in-Class) |
|---|---|---|
| **NRR** | Combined switching cost + pricing power + expansion | >120% enterprise; >130% exceptional |
| **GRR** | Pure switching cost depth | >90% enterprise; >95% mission-critical |
| **Gross Margin** | Competitive structure & reinvestment capacity | >80% top quartile SaaS; >70% acceptable |
| **Customer Concentration** | Moat breadth | No customer >10% ARR; top 10 <30% |
| **Implementation Time** | Proxy for switching cost | >3 months = meaningful depth |
| **Integration Count** | Technical switching cost depth | >10/customer = deeply embedded |
| **Contract Length** | Contractual lock-in | >2 years = strong signal |

**Diligence killer questions (customer reference calls):**
1. "What would it take for you to move to [Competitor]?"
2. "How many of your internal processes use [Vendor] data or workflows?"
3. "If [Vendor] doubled their price tomorrow, what would you do?"
4. "How many of your other tools connect to [Vendor]?"
5. "Have you ever formally evaluated switching? What stopped you?"

---

## 4. How AI Is Reshaping Software Moats

**Moats strengthening:** Proprietary workflow-embedded data, regulatory/compliance embedding, system-of-record position, data currencies.

**Moats weakening:** UI/UX differentiation, basic feature parity, data volume without feedback loop, scale as barrier to entry.

**The AI Agent Threat:** Most significant new erosion vector — agentic AI replacing point SaaS tools entirely. "Prompts are portable." Enterprise AI deployers reduced active SaaS vendor count by 31% within 18 months.

---

## 5. Composite Moat Scoring

```
Software_Moat = 0.30 * SC_Depth + 0.25 * DataNet + 0.20 * Expansion + 0.15 * Displacement + 0.10 * AI_Trajectory
```

| Score | Tier | CAP | PE Implication |
|---|---|---|---|
| 4.5-5.0 | Wide Moat | 15+ yr | Premium valuation. Underwrite price increases. |
| 3.5-4.4 | Narrow Moat | 7-15 yr | Standard PE. Moat deepening is the thesis. |
| 2.5-3.4 | Nascent Moat | 3-7 yr | Discount for moat risk. Execution-dependent. |
| <2.5 | No Moat | <3 yr | Avoid as platform investment. Growth story only. |

## 6. Pricing Model Vulnerability

| Score | Pricing Model | AI Resilience |
|---|---|---|
| 5 | Outcome/value-based or regulatory-mandated fee | Highest |
| 4 | Platform subscription with consumption upside | High |
| 3 | Hybrid (seat + consumption) | Medium |
| 2 | Pure per-seat/per-agent | Low |
| 1 | Per-minute/per-interaction in AI-automatable domain | Lowest |

If score <= 2: cap AI_Trajectory at 3. Require pricing pivot scenario in 100-Day Phase 5.

---

## Sources

- a16z: The Empty Promise of Data Moats
- NFX: Truth About Data Network Effects, 4 Types of Defensibility, Network Effects Manual, How AI Companies Build Real Defensibility
- Abraham Thomas: Data and Defensibility (Pivotal)
- Travis May: Six Moats of Data Businesses
- Hamilton Helmer: 7 Powers
- Greylock: The New New Moats (Jerry Chen)
- Morningstar Economic Moat Rating
- Morgan Stanley Counterpoint Global: Measuring the Moat
- Bain: Will Agentic AI Disrupt SaaS? (2025)
- S&P Global: Recalibrating the Competitive Moat
- PwC: AI Reshaping Software Valuations in M&A
