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

When the request names a product, product category, service, or service category and asks to analyze Ads Library, default to an **inventory-first** response. Identify all directly relevant distinct ads found in the accessible results, group them by advertiser page, deduplicate by Library ID, and report the number reviewed and retained. Do not impose an arbitrary 2-ad or 3–5-ad cap. “All” means all relevant distinct ads observed in accessible result cards for the stated scope, not all ads in Meta's database.

- Search the user's exact terms and a small, useful set of close variants/synonyms in the same language; preserve the requested country and active-status scope unless the user authorizes a change. Correct an obviously mismatched ad category only with a clear note (e.g., political/issues → all ads for ordinary products/services).
- Review result cards, not only keyword counts or advertiser suggestions. Continue through accessible result pages/cards when feasible. If the page is blocked, results are partial, or the browser cannot load further, say so and label the inventory partial; never imply exhaustive coverage.
- Include an ad only when the advertised offer directly sells, rents, books, or promotes the requested product/service, or directly solicits leads for it. Exclude incidental mentions, venues that merely contain the product, general businesses, and unrelated offers. Include adjacent products only if the user asked for the broader category; otherwise separate them as related-but-not-direct or omit them.
- For each relevant ad, capture page name (and page ID when visible), visible ad title or concise faithful hook/offer summary, one short useful point, and Library ID/direct link. Count unique pages separately from distinct ads and state both when possible. Keep product sales distinct from service offers.
- Include an ad only when the advertised offer directly sells, rents, books, or promotes the requested product/service, or directly solicits leads for it. Exclude incidental mentions, venues that merely contain the product, general businesses, and unrelated offers. Include adjacent products only if the user asked for the broader category; otherwise omit them or label them related-but-not-direct.
- Search exact terms and a small useful set of same-language variants/synonyms; preserve country and active-status scope unless authorized otherwise. Correct an obviously mismatched category only with a clear note. Review actual result cards, not only approximate search totals or suggested advertiser names.
- Continue through accessible result pages/cards when feasible. If blocked, incomplete, or unable to load further, label coverage partial and state what was actually reviewed. Never fabricate names, ad titles, IDs, or links; do not use approximate result totals as the relevant-ad count.
- Keep the inventory concise by shortening each ad description, not by omitting directly relevant ads. If the user explicitly requests only a shortlist or limit, follow it and state the selection rule.
- If more ads exist than can be reviewed in the available result view, list only actually inspected relevant ads and report the limitation; do not claim full-market completeness. Ask for a narrower category or time range only when that materially enables a useful inventory.

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
Use the structure in `templates/decision-memo.md`. Keep analysis and evaluation visibly separate:

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

- **Summary:** for general strategy questions, give the decision, 3–5 evidence-backed findings, 1–3 actions, and gaps. For product/service keyword discovery, group all directly relevant distinct ads actually inspected by page, using concise ad hooks, direct links, page/ad counts, and an honest scope/coverage note. Never impose a sample cap unless the user asks for one.
- **Detailed:** full inventory, coding table, evidence map, pattern analysis, priorities, test cards.
- **Product/service inventory:** concise grouped table of every directly relevant distinct ad reviewed (page, ad title/hook, useful point, direct Library link), followed by counts/scope/coverage and only the most useful cross-ad signals. Keep analysis short unless the user asks for detail.
- **Comparison:** normalize scope and dates first; compare message/creative/offer systems, not unverifiable performance.
- **Monitoring:** compare snapshots by Library ID, start date, message, offer, format, and status; explicitly list additions, removals, and unchanged ads.

## Ask at most three high-impact questions
Ask only when the missing answer would change the recommendation: target country/status, user's offer and business goal, and whether performance/export data exists. Otherwise proceed with stated assumptions.
