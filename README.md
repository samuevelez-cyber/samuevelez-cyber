## Sam Velez

**I build the AI systems that run Amazon ad operations.**

7+ years in Amazon advertising. Currently at **Emplicit**, managing a five-brand portfolio — roughly $300K/month in ad spend, ~$1.4M/month in revenue — on top of an agentic automation suite I designed and maintain.

Most people in performance marketing use AI as a chatbot. I build the systems that run the operation.

---

### What I've built

**An 18-skill agentic PPC system** · 38 Python scripts, ~14,600 lines

Runs the weekly optimization cycle end to end across a ~$3.6M/yr ad portfolio:

1. **Ingest & reconcile** — bulk exports joined across 7/30/60-day windows and stacked weeklies, so no decision rests on one noisy week. Entity IDs reconciled so a keyword is tracked continuously across exports.
2. **Classify** — every campaign, keyword, and product target scored against a quantitative tier framework relative to its own target, with account posture and promotional windows applied first.
3. **Propose** — a specific action per flagged entity, each carrying the evidence that triggered it and the rule it came from.
4. **Stop.** Nothing executes. The output is a plan a human reviews, edits, and approves.
5. **Build** — the upload file is generated from the approved plan, never from the system's own recommendations.
6. **Verify** — next cycle, shipped changes are diffed against the new export and anything that didn't hold gets flagged.

The design principle: **automation should compress the analysis, not take the judgment.** The system is good at what people are bad at — holding a thousand entities in view, applying a rule consistently, remembering what shipped three weeks ago and whether it stuck. It's bad at knowing a client is launching next month. So it does the first job and hands over the second.

Every recommendation arrives with its evidence attached, which makes review fast and disagreement easy. That's what keeps a reviewer actually reviewing instead of rubber-stamping by week three.

---

**A quantitative decision framework** · adopted as Emplicit's optimization standard

Ask three PPC managers what to do with a keyword at 62% ACoS against a 30% target and you'll get three defensible answers. That inconsistency is invisible day to day and expensive over a quarter.

- **Performance tiers** — classification by actual ACoS relative to target, not absolute numbers, which mean nothing across accounts with different margins.
- **Bid math with brakes** — target bids derive from the entity's own economics (revenue per click × target ACoS), then dampen toward current and hard-cap at ±50% per adjustment. Bids move toward correct at a pace that doesn't whipsaw the auction.
- **A zero-order ladder** — entities that spend without converting have no ACoS to compute against, so they walk a graduated ladder instead, each rung requiring a fresh trigger's worth of evidence.
- **Posture modifiers** — growth and defensive accounts shouldn't treat the same keyword identically. Detected from trailing performance, applied before classification.
- **Evidence gates** — the most important rules are the ones about when *not* to act. Minimum thresholds scaled to the account's own clicks-per-order, multi-window agreement checks, promotional-window flags forcing corroboration against clean data.

It doesn't remove judgment. It makes judgment explicit enough to argue with.

---

**A personal multi-agent system** · because the ideas should survive outside work

An always-on self-hosted assistant reachable from chat, with memory that persists across devices; a local model handling extraction and research fan-out so cheap work stays cheap; scheduled briefings; scoped memory isolation so separate contexts can't read each other. It's how I find out which agent-architecture ideas survive daily use. Most don't.

---

### Results

| | |
|---|---|
| TACOS held at **11.3%** against a 15% target | ~**$32K/week** in sales recovered after a Buy Box diagnosis |
| Managed ACoS at **35%** on a 45% target | ~22% headroom reinvested into growth |
| **~$4K/week** in efficiency savings | from a single 4-week aggregate audit |
| **129 → 13** campaigns | portfolio restructure |
| **40% → 20%** ACoS | freelance client, volume held |

*Client identities withheld under agency confidentiality. Figures are portfolio aggregates.*

---

### Stack

`Python` · `Claude (Agent Skills, MCP)` · `Amazon Ads bulk operations` · `JSON schema contracts` · `append-only action ledgers` · `Helium 10` · `Intentwise`

**Certified:** Claude API · Claude Code · Model Context Protocol · Agent Skills · Claude Cowork

---

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/samuel-velez-palacio-550516155/) · [Upwork](https://www.upwork.com/freelancers/~016314380c9ef6fd54) · [X](https://x.com/samuevelez)

Medellín, Colombia · remote · **samuevelez@gmail.com**

Open to AI/automation and AI-enabled marketing roles, and to consulting projects — particularly with teams running ads at scale on a fully manual optimization process.