# Choosing a flagship model

A decision guide for picking among the top-tier models in this list (as of September 2026). Prices and standings change fast — verify on the vendor's page before committing.

## By workload

**Agentic coding / software engineering**
- Best overall: **Claude Fable 5.1** (TB 4.0 55.8%, CursorBench 73.4%) or **GPT-6 Astra** (TB 4.0 57.9%, computer-use SOTA) — both $10/$50.
- Best value coding: **Kimi K3** ($3/$15, open weights) or **Grok 4.7** ($2/$6, DeepSWE 71%).
- Budget coding: **DeepSeek V4 Pro** (off-peak $0.66/$1.98) or **step-3.7-flash** ($0.20/$1.15, Apache 2.0).

**Computer use / OS automation**
- **GPT-6 Astra** is the category leader (OSWorld 2.0 72.6%, ARC-AGI-3 99.9%). Fable 5.1 is the alternative (OSWorld 77.9% partial).

**Long-context document work (1M+ tokens)**
- **Gemini 3.1 Pro**, **DeepSeek V4 Pro**, **Kimi K3**, **MiMo-V2.6-Pro**, **MiniMax M3**, **Nemotron 3 Ultra**, **Hy4 Preview** all offer ~1M context. Gemini has the deepest Workspace/Search integration; DeepSeek is cheapest.

**Scientific / research work**
- **Claude Fable 5.1** (TB-Science 52.6%) and **GPT-6 Astra** (TB-Science 64.6%, FrontierMath Tier 4 98%) lead.

**Multilingual / enterprise knowledge work**
- **Command A+** (48 languages, RAG focus), **Mistral Large 3** (80+ languages, GDPR-friendly EU hosting).

**China-market deployment**
- **ERNIE 5.1** (Baidu ecosystem), **Qwen3.8-Max** (Alibaba Cloud), **Doubao-Seed-2.1 Pro** (ByteDance products) — check data-residency requirements.

**Self-hosting / data control**
- See [Open-weight flagships](../README.md#open-weight-flagships) in the README. **Mistral Large 3** and **MiMo-V2.6-Pro** have the most permissive licenses (Apache 2.0 / MIT). **GLM-5.3** and the Qwen checkpoint carry custom licenses — read before commercial use. **Nemotron 3 Ultra** is commercial-license open weights.

## Price tiers (per 1M in/out, verified where marked)

| Tier | Models |
|---|---|
| $10/$50 | GPT-6 Astra ✅, Claude Fable 5.1 ✅ |
| $2–$4/$6–$18 | Grok 4.7 ✅, Gemini 3.1 Pro ✅, Kimi K3 ✅, Qwen3.8-Max ⚠️, GLM-5.3 ⚠️ |
| Sub-$1.50 in | Mistral Large 3 ✅ $0.50/$1.50, MiMo-V2.6-Pro ⚠️ $0.435/$0.87, MiniMax M3 ⚠️ $0.30/$1.20, DeepSeek V4 Pro ⚠️ $0.66/$1.98 off-peak, step-3.7-flash ⚠️ $0.20/$1.15, ERNIE 5.1 ⚠️ $0.59/$2.65, Hy3 ⚠️ $0.15/$0.59, Hy4 Preview ⚠️ $0.834/$2.501, Muse Spark 1.3 ⚠️ $1.25/$4.25, Nova 2 Lite ⚠️ $0.30/$2.50 |
| Unknown | Command A+, Nova 2 Pro (preview), MAI-Thinking-1 (preview), Nemotron 3 Ultra, Seed-2.1 Pro (CNY only) |

**Rule of thumb:** if your workload is token-heavy and agentic, cache-read pricing (Fable 5.1: $0.25 vs $10 input) and off-peak windows (DeepSeek) can cut effective cost 25–75% below the sticker price.

## Avoid

- Quoting prices for the five "unknown" flagships — there is no public per-token figure; ask the vendor.
- Assuming announced models are shipping: Gemini 3.5 Pro and Qwen 4 Max were both announced but unreleased at the Sept 29, 2026 cutoff.
- Treating vendor benchmarks as independent — see [benchmarks-notes.md](benchmarks-notes.md).
