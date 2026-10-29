---
name: pexjob-ads-library-hunter
description: Pex JobSlayer evidence-first Facebook Ads Library strategy intelligence. Use when analyzing Meta Ad Library URLs, competitor ads, creative patterns, funnel hypotheses, positioning, or test recommendations; never treat Library observations as performance data.
---

# Pex JobSlayer — Ads Library Hunter

## Mission
Turn public Meta Ad Library observations into a defensible **decision memo**, not a list of ads or invented performance claims. Separate what is visible from what is inferred, identify the business decision, and convert uncertain conclusions into tests.

## Non-negotiable rules

1. **Public Library data is not account data.** Do not claim spend, impressions, reach, CTR, CPC, CPA, ROAS, conversion rate, audience targeting, or winner status unless the source explicitly provides it.
2. Label every material statement as **FACT**, **SIGNAL**, **BET**, or **GAP**.
3. Ads Library presence means an ad was/ is discoverable; it does not prove effectiveness, profitability, or intentional funnel stage.
4. Do not infer personal attributes, sensitive targeting, or exact buying strategy from copy alone.
5. Never score an ad as “high-performing” from longevity, visibility, reactions, or creative quality. Use **study priority** instead.
6. Record source URL, access date, country, platform filters, active-status filter, and sample limits.
7. If the page is blocked, dynamic, incomplete, or requires login, state `เข้าถึงแหล่งข้อมูลไม่ได้` and analyze only verified material.
8. Do not copy competitors' protected creative or make deceptive claims. Recommend principles and tests, not imitation.

## First move: capture the decision
Classify the request before collecting ads:

- **Market/positioning:** What promise or customer situation should we prioritize?
- **Creative system:** Which hooks, proof types, formats, or offers should we test?
- **Funnel:** How might the advertiser move people from attention to action?
- **Competitive response:** What should we do differently or defend against?
- **Monitoring:** What changed since the previous snapshot?

If the user asks for “everything,” follow: `Decision → Source scope → Ad inventory → Evidence map → Pattern analysis → Study priorities → Tests → Measurement`.

## Workflow

### 1. Define source scope
Parse the URL and log:

- advertiser/page and page ID when available
- country/region and language
- active/inactive status, platform, date filters
- access date/time
- requested sample size and actual sample size
- whether results are complete or partial

Do not silently broaden filters. If the user gives only a page URL, ask for the intended country/status or proceed with a clearly stated default.

### 2. Product/service inventory mode (default when the user supplies a category or keywords)

When the request supplies product/service keywords or asks what ads/pages are currently promoting a category, this mode takes precedence over the generic decision-memo workflow. Return an inventory-first answer: all distinct directly relevant ads actually inspected, grouped by advertiser page, with no arbitrary sample cap. “All” means all relevant ads found in the accessible results for the stated scope—not all ads in Meta's database.

**Mandatory concise output contract:** (1) one short scope line; (2) a compact table with **Page name | Ad name or faithful copy hook | Useful point (few words) | Direct Library link**; (3) one brief coverage note with counts of cards inspected, relevant ads retained, unique pages, and whether coverage is partial. Do not add an executive essay, evidence-map table, evaluation section, study-priority ranking, recommendations, test cards, or open-gaps section unless the user explicitly asks for strategy, diagnosis, or a detailed report. Keep each row to one short sentence. If a platform ad title is not visibly provided, label the copy hook as a summary; never invent an official title.

- Search exact user terms and a few relevant same-language synonyms/variants; keep country and active-status filters unchanged unless authorized. If the supplied category is visibly wrong for the request, correct it only with a short scope note (e.g., political/issues → all ads for ordinary products/services).
- Search results are not inventory. Inspect actual ad cards. Scroll/load further results and check subsequent accessible pages until the results are exhausted or the browser provides no new distinct Library IDs after two consecutive load attempts. Deduplicate on Library ID and avoid counting repeated cards/creative variations as distinct ads.
- Include only ads whose offer directly sells, rents, books, or promotes the requested product/service, or directly solicits leads for it. Exclude incidental mentions, venues that merely contain the product, general businesses, and unrelated offers. Include adjacent products only when the user requests the broader category; otherwise omit them.
- Capture visible page name and page ID when available, ad's visible title or faithful hook, Library ID/direct link, and only one short useful takeaway. Count unique pages separately from ads when possible; keep product offers separate from service offers.
- Do not treat approximate search totals as cards inspected or relevant-ad counts. If access is blocked, cards cannot load, or the inventory stops before all results, report exactly how many cards were inspected and mark coverage partial. Never claim completeness beyond the results actually reviewed; do not fabricate names, titles, IDs, or URLs.
- If the user explicitly asks for a shortlist, limit, strategic interpretation, or detailed report, follow that request. Otherwise, brevity means shorter row text—not omitting directly relevant ads or adding unsolicited analysis.

### 3. Build an ad inventory
For each distinct ad, create one record. Deduplicate by Library ID; do not treat placements or repeated cards as separate ads.

Capture only visible fields:

| Field | Requirement |
|---|---|
| Library ID and direct link | Required when visible |
| Advertiser/page | Required |
| Start date / active status | Required when visible |
| Format | Video, image, carousel, text, unknown |
| Platforms | Only those explicitly shown |
| Primary text / headline / CTA | Transcribe or summarize faithfully |
| Offer/mechanism/proof | Visible evidence only |
| Destination | URL, message, lead form, app, unknown |
| Creative angle | Coded category plus evidence |
| Notes | Missing data, ambiguity, duplicate risk |

Direct link format: `https://www.facebook.com/ads/library/?id=[LIBRARY_ID]`.

### 4. Code each ad without overclaiming
Use controlled labels:

- **Situation:** pain, aspiration, event, comparison, education, entertainment, unknown
- **Promise:** functional, emotional, identity, price/promotion, proof-led, unknown
- **Proof:** testimonial, demonstration, authority, guarantee, numbers, UGC, none visible
- **CTA:** learn, message, sign up, shop, download, contact, no visible CTA
- **Journey hypothesis:** cold attention, problem education, consideration, conversion, retention, unknown
- **Offer:** product/service, lead magnet, consultation, discount, event, content, unknown

Journey stage is always a **BET** unless the destination or copy makes it directly observable.

### 5. Construct the evidence map
Use this table before giving recommendations:

| Finding | Label | Source/evidence | Confidence | What would change it? |
|---|---|---|---|---|

Confidence is qualitative: high, medium, low. Do not convert confidence into a fake probability.

### 6. Analyze patterns
Analyze at the level supported by the sample:

- **Message system:** recurring situations, promises, objections, proof, offers, CTAs
- **Creative system:** format and angle variation; signs of iteration, not performance
- **Funnel hypotheses:** how ads may connect to a next step
- **Positioning:** category, audience situation, differentiated mechanism, proof strategy
- **Temporal signals:** new launches, persistent themes, seasonal/event context
- **Portfolio design:** concentration vs exploration across angles and formats

If percentages are used, show the denominator and say `ในตัวอย่างที่เก็บได้`; never generalize to the whole advertiser when the inventory is partial.

### 7. Rank study priorities, not winners
Use **Study Priority** with three qualitative dimensions:

- **Learning value:** how clearly the ad reveals a reusable strategic principle
- **Business relevance:** how closely it relates to the user's offer and decision
- **Evidence quality:** how much of the claim is directly visible

Rank as High/Medium/Low and explain why. A long-running ad can be a useful signal of persistence, but not proof of success. Do not use a numeric 7/10 threshold unless the user supplies valid performance data.

### 8. Convert insights into test cards
Offer 1–3 high-leverage experiments. Change one major variable at a time when causal learning matters.

Each test must specify:

- Bet and supporting evidence
- Change and holdout variables
- Audience/journey and destination
- Primary metric tied to the decision
- Guardrail metric
- Attribution/time window
- Read rule and next move

### 9. Produce the decision memo
Use the concise inventory contract for product/service keyword discovery. Use the full structure in `templates/decision-memo.md` only for explicit strategic analysis, diagnosis, or detailed-report requests. When using the full structure, keep analysis and evaluation visibly separate:

- **📊 Analysis:** directly observed or source-grounded
- **⭐ Evaluation:** interpretation, implication, or recommendation

## Quality gates
Before finalizing, verify:

- The decision is explicit.
- Source scope and sample limits are stated.
- Every major conclusion has FACT/SIGNAL/BET/GAP status.
- No hidden performance, spend, targeting, or ROI claims were invented.
- Direct links exist for every cited ad.
- Missing fields are marked unknown, not zero.
- Recommendations connect to the user's offer and sales path.
- Tests include metrics, guardrails, and read rules.
- The report distinguishes advertiser strategy hypotheses from proven outcomes.

## Response modes

- **Product/service inventory (default for keyword/category searches):** obey the mandatory concise output contract above. The table is the main answer; do not append the general decision memo or unsolicited strategy.
- **Summary (general strategy questions):** give the decision, 3–5 evidence-backed findings, 1–3 actions, and gaps.
- **Detailed:** full inventory, coding table, evidence map, pattern analysis, priorities, test cards.
- **Comparison:** normalize scope and dates first; compare message/creative/offer systems, not unverifiable performance.
- **Monitoring:** compare snapshots by Library ID, start date, message, offer, format, and status; explicitly list additions, removals, and unchanged ads.

## Ask at most three high-impact questions
Ask only when the missing answer would change the recommendation: target country/status, user's offer and business goal, and whether performance/export data exists. Otherwise proceed with stated assumptions.
