---
name: pexjob-ads-library-hunter
description: "Search and analyze Meta Ads Library ads. Use first for product/service keyword searches: inspect every supplied term, list all distinct directly relevant ads actually found, and state coverage. Also use for competitor creative, positioning, funnel hypotheses, and strategy; never treat Library observations as performance data."
---

# Pex JobSlayer — Ads Library Hunter

## Mission
Turn public Meta Ad Library observations into accurate, decision-useful output. For product/service keyword searches, the primary deliverable is the complete concise inventory of distinct, directly relevant ads actually inspected—not a decision memo, shortlist, or sample. For explicit strategy requests, provide a decision memo. Never invent performance claims.

## Non-negotiable rules

1. **Public Library data is not account data.** Do not claim spend, impressions, reach, CTR, CPC, CPA, ROAS, conversion rate, audience targeting, or winner status unless the source explicitly provides it.
2. In strategy/diagnosis mode, label material statements as **FACT**, **SIGNAL**, **BET**, or **GAP**. Do not add these labels to a simple inventory table unless requested.
3. Ads Library presence means an ad was/ is discoverable; it does not prove effectiveness, profitability, or intentional funnel stage.
4. Do not infer personal attributes, sensitive targeting, or exact buying strategy from copy alone.
5. Never score an ad as “high-performing” from longevity, visibility, reactions, or creative quality. Use **study priority** instead.
6. Record source URL, access date, country, platform filters, active-status filter, and sample limits.
7. If the page is blocked, dynamic, incomplete, or requires login, state `เข้าถึงแหล่งข้อมูลไม่ได้` and analyze only verified material.
8. Do not copy competitors' protected creative or make deceptive claims. Recommend principles and tests, not imitation.

## First move: capture the decision
Classify the request before collecting ads. **If the user supplies product/service keywords or asks what advertisers are promoting, choose Product/service inventory mode and do not run the generic decision-memo workflow.**

- **Market/positioning:** What promise or customer situation should we prioritize?
- **Creative system:** Which hooks, proof types, formats, or offers should we test?
- **Funnel:** How might the advertiser move people from attention to action?
- **Competitive response:** What should we do differently or defend against?
- **Monitoring:** What changed since the previous snapshot?

Use `Decision → Source scope → Evidence map → Pattern analysis → Study priorities → Tests → Measurement` only when the user explicitly requests strategy, diagnosis, or a detailed report. A product/service keyword request gets the inventory contract below, even when phrased broadly as “analyze these ads.”

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

**Mandatory concise output contract:** (1) one short scope line; (2) a compact table with **Page name | Ad name or faithful copy hook | Library ID / direct link**; (3) one brief coverage note with the unique relevant-ad count, visible page-name count, and whether coverage is partial. State how many user terms were searched, and list each term's approximate result total and inspected-card count when available. Do not add an executive essay, evidence-map table, evaluation section, study-priority ranking, recommendations, test cards, or open-gaps section unless the user explicitly asks for strategy, diagnosis, or a detailed report. Keep each row to one short faithful hook. If a platform ad title is not visibly provided, label the copy hook as a summary; never invent an official title.

**Do not submit a sample as if it were the inventory.** Before responding, verify that the final table includes every directly relevant distinct Library ID actually inspected across every supplied query. The table row count must equal the stated unique relevant-ad count. If the user did not ask for a shortlist, never return “top examples,” a few representative rows, or only the first visible cards. If the browser or response limit prevents completion, say exactly what remains uninspected and mark the result partial; include all inspected relevant ads in a complete attached file when the list is long.

**Mandatory execution gate — complete this before drafting the answer:**
1. Parse and record the user's keywords as a numbered list. Treat each space-separated product phrase as its own search when multiple phrases are supplied; never replace the list with one broad word. For example, `ตู้อบซาวน่า เครื่องอบซาวน่า ห้องซาวน่า ซาวน่าสำเร็จรูป ซาวน่าอินฟราเรด` means five queries.
2. Run each exact phrase separately. Do not mark a query complete until Ads Library's search field or URL visibly contains that phrase and the result cards have been reviewed. Maintain a completed/skipped status for every phrase.
3. For each query, note the approximate result total if shown, inspect the loaded cards, and scroll **the result list** (not just the page footer) to load more. Repeat while new Library IDs appear; stop only at the end or after two consecutive load attempts add no new IDs. If the browser cannot scroll/load, state the specific limitation and leave that query partial/blocked.
4. Merge all inspected cards, deduplicate by Library ID, and classify direct relevance. Before answering, verify all supplied terms have a completed or explicitly blocked status and that table rows equal the unique relevant-ID count. Never silently omit a term, card, or excess rows.

- Search **every product/service term explicitly supplied by the user as its own query**; do not let one broad term stand in for the others. Search exact phrases first, then add only useful close variants if needed. Preserve country, active status, and other requested filters. If the URL's ad category is mismatched to ordinary products/services (e.g., political/issues), switch to all ads and state this briefly.
- Maintain one query log: each term, Ads Library's approximate result total if displayed, distinct card IDs actually inspected, and any loading/access limit. Search totals are not the inspected count. Do not stop after the first keyword or first few cards merely because results are numerous.
- For each query, inspect actual ad cards, scroll/load further results, and continue until results are exhausted or two consecutive load attempts yield no new distinct Library IDs. Combine the query results, deduplicate globally by Library ID, and do not count repeated placements or the same ad returned under multiple keywords twice.
- Include only ads whose offer directly sells, rents, designs, installs, repairs, or promotes the requested product/service, or directly solicits leads for it. Exclude incidental mentions, venues that merely contain the product, general businesses, and unrelated offers. Include adjacent formats only when they fit an explicitly supplied umbrella term; label the product type so a sauna blanket is not mistaken for a sauna cabin/room.
- Capture visible page name (and page ID when shown), visible ad title or faithful short copy hook, Library ID, and direct link. Do not invent official ad titles. Count unique page IDs where visible; otherwise report the number of distinct visible page-name labels, not a guaranteed number of unique businesses.
- For the default inventory mode, these are the only required row fields. Use the larger record schema and creative coding below only when the user asks for strategy, comparison, or a detailed report.
- Never infer completeness from approximate result totals. If any query's cards cannot be exhausted, report the exact per-query inspection coverage and mark the combined inventory partial. Never fabricate names, titles, IDs, or URLs.
- Do not impose an arbitrary ad-count cap. If the complete relevant inventory is too long for a readable chat response (e.g., more than 25 distinct ads), save the **entire** concise table as a Markdown or CSV attachment and give only the scope, unique counts, coverage caveat, and file link in chat; never replace it with a shortlist. For smaller inventories, show the full table directly.
- If the user explicitly asks for a shortlist, limit, strategic interpretation, or detailed report, follow that request. Otherwise, shorten each row rather than omitting directly relevant ads or adding unsolicited analysis.

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
Use this section only for explicit strategy, diagnosis, comparison, or detailed-report requests; skip it for keyword inventory. When applicable, analyze at the level supported by the sample:

- **Message system:** recurring situations, promises, objections, proof, offers, CTAs
- **Creative system:** format and angle variation; signs of iteration, not performance
- **Funnel hypotheses:** how ads may connect to a next step
- **Positioning:** category, audience situation, differentiated mechanism, proof strategy
- **Temporal signals:** new launches, persistent themes, seasonal/event context
- **Portfolio design:** concentration vs exploration across angles and formats

If percentages are used, show the denominator and say `ในตัวอย่างที่เก็บได้`; never generalize to the whole advertiser when the inventory is partial.

### 7. Rank study priorities, not winners
Use **Study Priority** with three qualitative dimensions only in explicit strategy/detailed-report mode:

- **Learning value:** how clearly the ad reveals a reusable strategic principle
- **Business relevance:** how closely it relates to the user's offer and decision
- **Evidence quality:** how much of the claim is directly visible

Rank as High/Medium/Low and explain why. A long-running ad can be a useful signal of persistence, but not proof of success. Do not use a numeric 7/10 threshold unless the user supplies valid performance data.

### 8. Convert insights into test cards
Offer 1–3 high-leverage experiments only when requested or when the user explicitly asks for strategy. Change one major variable at a time when causal learning matters.

Each test must specify:

- Bet and supporting evidence
- Change and holdout variables
- Audience/journey and destination
- Primary metric tied to the decision
- Guardrail metric
- Attribution/time window
- Read rule and next move

### 9. Produce the decision memo
For product/service keyword discovery, search every supplied term separately, merge results by Library ID, and use the concise inventory contract. If over 25 distinct ads are found, save and attach the complete short table rather than truncating it. Use the full structure in `templates/decision-memo.md` only for explicit strategic analysis, diagnosis, or detailed-report requests. When using the full structure, keep analysis and evaluation visibly separate:

- **📊 Analysis:** directly observed or source-grounded
- **⭐ Evaluation:** interpretation, implication, or recommendation

## Quality gates
Before finalizing, verify:

- In inventory mode, every supplied query has a status, each inspected direct ad is listed once, and row count equals unique relevant Library IDs.
- In strategy mode, the decision is explicit and source scope/sample limits are stated.
- In strategy mode, material conclusions have FACT/SIGNAL/BET/GAP status.
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
