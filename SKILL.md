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

When the request names a broad product/service category or keywords and the user's main goal is market/competitor discovery, default to **page-first market inventory**, not a long ad-by-ad dump. Identify distinct advertiser pages with directly relevant offers, deduplicate pages by page ID when available (otherwise normalize visible page names and flag ambiguity), and report the number of unique relevant pages observed. Show at most two representative ads per page, deduplicated by Library ID, with direct links and concise hooks. “Observed pages” means pages found in accessible result cards, not all competitors in the market.

When the user explicitly asks for a complete ad inventory, or has selected a page for deep dive, identify all distinct relevant ads visible for that scope and report the count reviewed. Never impose a two-ad cap in a requested single-page deep dive; the two-ad limit applies to broad market-discovery summaries only.

- Search the user's exact terms and a small, useful set of close variants/synonyms in the same language; preserve the requested country and active-status scope unless the user authorizes a change. Correct an obviously mismatched ad category only with a clear note (e.g., political/issues → all ads for ordinary products/services).
- Review result cards, not only keyword counts or advertiser suggestions. Continue through accessible result pages/cards when feasible. If the page is blocked, results are partial, or the browser cannot load further, say so and label the inventory partial; never imply exhaustive coverage.
- Include an ad only when the advertised offer directly sells, rents, books, or promotes the requested product/service, or directly solicits leads for it. Exclude incidental mentions, venues that merely contain the product, general businesses, and unrelated offers. Include adjacent products only if the user asked for the broader category; otherwise separate them as related-but-not-direct or omit them.
- In market-discovery mode, group results by advertiser page and show no more than two representative ads per page; capture page name, page ID when visible, each ad's faithful hook/offer summary, Library ID/direct link, and one short useful observation. Count pages separately from ads and state both counts when possible. Keep product sales distinct from service offers.
- After a broad market-discovery summary, offer clear next-step choices: **เจาะลึกเพจ** (ask the user to type/select a page name; then count its currently visible active ads and analyze offers, formats, proof, CTA, and useful strategic signals) and **วิเคราะห์คอนเทนต์** (analyze messaging themes, hooks, proof, objections, formats, and testable content ideas for the market or selected page). Present these as selectable choices where the interface supports it; otherwise use a numbered choice prompt. Do not claim a button exists if it cannot actually be rendered.
- If more ads are found than can be reviewed in the available result view, list only the actually inspected relevant ads and state the limitation; do not fabricate missing names, ad titles, IDs, or links. Do not use approximate result totals as the number of relevant ads.
- In broad category discovery, the user's default is page count first and at most two sample ads per page. If the number of pages cannot reasonably be reviewed in the accessible result view, report the inspected page count and limits rather than asking for an arbitrary ad limit. In full-inventory or page-deep-dive mode, follow the user's requested scope and report partial coverage honestly.

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

- **Summary:** for general strategy questions, give the decision, 3–5 evidence-backed findings, 1–3 actions, and gaps. For broad product/service category discovery, use page-first market inventory: unique relevant page count, up to two representative ads per page, scope/limits, and the two next-step choices (page deep dive or content analysis). For explicit complete-inventory requests, list all relevant distinct ads actually inspected.
- **Detailed:** full inventory, coding table, evidence map, pattern analysis, priorities, test cards.
- **Product/service inventory:** concise table of every directly relevant distinct ad reviewed (page, ad title/hook, useful point, direct Library link), followed by a brief count/scope note and only the most useful cross-ad signals. Keep analysis short unless the user asks for detail.
- **Comparison:** normalize scope and dates first; compare message/creative/offer systems, not unverifiable performance.
- **Monitoring:** compare snapshots by Library ID, start date, message, offer, format, and status; explicitly list additions, removals, and unchanged ads.

## Ask at most three high-impact questions
Ask only when the missing answer would change the recommendation: target country/status, user's offer and business goal, and whether performance/export data exists. Otherwise proceed with stated assumptions.
