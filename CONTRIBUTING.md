# Contributing to Awesome Flagship LLMs

Thanks for helping keep this list accurate. Flagship models change fast — prices, context windows, and model names move monthly — so corrections are the most valuable contribution.

## What belongs here

- A lab's **single most capable general-purpose model**. If a lab's top model is unclear, say so in the PR.
- Announced-but-unshipped models are **not** entries; they go in `docs/status-changes.md`.
- Retired models are **not** entries; they go in `docs/status-changes.md` and the README's retired table.
- Efficiency tiers (flash/mini/haiku/nano), free tiers, image-only, embedding, and moderation models are out of scope — see the sibling lists.

## Adding an entry

1. Edit `data/flagship-llms.json` — add one object following the schema below, and insert it in the lab's section order in `README.md`.
2. Keep entries factual and neutral. No marketing copy, no comparisons in the entry text.

### Schema

```json
{
  "name": "Model Name",
  "vendor": "Lab Name",
  "url": "https://official-model-or-docs-page",
  "description": "One neutral sentence: what it is and what it's for.",
  "price_input_per_1m": "$10",
  "price_output_per_1m": "$50",
  "price_verified": true,
  "pricing_url": "https://official-pricing-page",
  "status": "active",
  "category": "flagship",
  "features": ["1M-token context", "Open weights (Apache 2.0)", "..."]
}
```

Field rules:

- `url` must be the vendor's official page (model announcement, docs, or product page).
- Prices are strings like `"$0.50"` or `"unverified"`. For tiered pricing, write both tiers in the string (see Gemini 3.1 Pro). **Never guess a price** — use `"unverified"`, `price_verified: false`, and `pricing_url: ""`.
- `price_verified: true` **only** if you read the number on the vendor's official pricing page or official announcement. Read date goes in the README entry (✅ verified YYYY-MM-DD).
- `status`: `active` (GA), `commercial` (preview-gated / enterprise), `beta`/`deprecated` as needed.
- Keep `features` to 6 items max: context window, architecture, license, benchmarks, availability notes.

## Pricing changes

Update `price_input_per_1m` / `price_output_per_1m`, flip `price_verified` to `true` only if re-read officially, update the README badge date, and add a row to `docs/status-changes.md`.

## Retirements / renames

Move the entry out of `data/flagship-llms.json` and `README.md`; add a row to the retired table in `README.md` and an entry in `docs/status-changes.md`.

## Checks

CI validates:
- JSON parses and all fields are present with the right types.
- No duplicate names. (Sibling models from one lab may share an official page URL.)
- All `url` / `pricing_url` start with `https://`.
- `status` is one of `active`, `beta`, `deprecated`, `commercial`; `category` is `"flagship"`.
- `price_verified` is a boolean; verified entries must have an https `pricing_url`, unverified entries leave it empty.
- All Markdown links in `README.md`, `CONTRIBUTING.md`, and `docs/` resolve (lychee), ignoring known-blocked hosts.
