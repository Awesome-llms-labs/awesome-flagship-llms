# Awesome Flagship LLMs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated directory of **flagship LLMs** — the single most capable model from every major AI lab, as of **September 2026**. This is the top tier only: not the flash/mini/haiku efficiency lines (see [awesome-flash-llms](https://github.com/dakotac1994/awesome-flash-llms)), not the free tiers (see [awesome-free-llms](https://github.com/dakotac1994/awesome-free-llms)) — the models the labs put forward as their best.

The flagship race in 2026 is a story of convergence and divergence: OpenAI's **GPT-6 Astra** and Anthropic's **Claude Fable 5.1** both landed at **$10/$50** per 1M tokens in September, while open-weight flagships like **DeepSeek V4 Pro**, **Kimi K3**, and **MiMo-V2.6-Pro** push frontier-class intelligence at 1–2 orders of magnitude less. Meanwhile Google's **Gemini 3.5 Pro was announced but never shipped** — the 3.1 Pro holds the line — and preview-gated models (Nova 2 Pro, MAI-Thinking-1, Hy4) keep their pricing under wraps.

**Pricing confidence:** every price below is stamped ✅ **verified 2026-09-30** (read on the vendor's official pricing page or official announcement) or ⚠️ **unverified** (third-party or stale). **Prices are never guessed.** Five flagships (Cohere Command A+, Nova 2 Pro, MAI-Thinking-1, Nemotron 3 Ultra, and the ByteDance CNY-only listing) have no usable public per-token price — those say so explicitly. Machine-readable records live in [`data/flagship-llms.json`](data/flagship-llms.json) with a `price_verified` boolean per entry.

## 2026 Highlights

- **OpenAI GPT-6 Astra** (Sept 3): state-of-the-art computer use and science; first model rated "Critical" for cyber under the Preparedness Framework. ✅ $10 in / $50 out. DevDay (Sept 29) launched **GPT-6.1 Sol** at $2/$10 — near-flagship at 1/5 the cost.
- **Anthropic Claude Fable 5.1** (Sept 1): "most capable generally available model"; ~25–45% cheaper typical workloads than Fable 5 via cache-read cuts. ✅ $10/$50.
- **xAI Grok 4.7** (Sept 21): 2.1T params, DeepSWE 71.0% at xHigh. ✅ $2/$6 (<200K prompt).
- **Google's Pro tier stalled**: Gemini 3.5 Pro announced at I/O but never shipped; 3.1 Pro remains flagship. ✅ $2/$12 (≤200K).
- **Open-weight wave**: Kimi K3 (2.8T, ✅ $3/$15), MiMo-V2.6-Pro (AA Index 46, #1 open-weight), DeepSeek V4 Pro (off-peak $0.66/$1.98), Mistral Large 3 (Apache 2.0, ✅ $0.50/$1.50).
- **Retirements**: Nova Premier EOL'd (Sept 14), Kimi K2.5 retired (Aug 31), Grok 4.6 → 4.7, GLM-5.x → 5.3, Seed 2.0 → 2.1 Pro. DeepSeek's planned V4-Pro sunset was **cancelled**.

## Contents

- [Flagship models](#flagship-models)
  - [OpenAI](#openai)
  - [Anthropic](#anthropic)
  - [Google DeepMind](#google-deepmind)
  - [xAI](#xai)
  - [DeepSeek](#deepseek)
  - [Alibaba — Qwen](#alibaba--qwen)
  - [Zhipu AI — GLM](#zhipu-ai--glm)
  - [Moonshot AI — Kimi](#moonshot-ai--kimi)
  - [MiniMax](#minimax)
  - [Mistral AI](#mistral-ai)
  - [Cohere](#cohere)
  - [Amazon — Nova](#amazon--nova)
  - [Meta](#meta)
  - [Baidu — ERNIE](#baidu--ernie)
  - [StepFun](#stepfun)
  - [Xiaomi — MiMo](#xiaomi--mimo)
  - [Microsoft](#microsoft)
  - [NVIDIA — Nemotron](#nvidia--nemotron)
  - [Tencent — Hunyuan](#tencent--hunyuan)
  - [ByteDance — Doubao/Seed](#bytedance--doubao-seed)
- [Open-weight flagships](#open-weight-flagships)
- [Benchmarks & eval notes](#benchmarks--eval-notes)
- [Retired & superseded flagships (2026)](#retired--superseded-flagships-2026)
- [Guides](#guides)
- [Contributing](#contributing)
- [License](#license)

---

## Flagship models

### OpenAI

- [GPT-6 Astra](https://openai.com/index/gpt-6-astra/) — ✅ **$10 in / $50 out** (cached $1.00; Batch/Flex $5/$25). 1.05M context / 128K output; cutoff 2026-04-30. GA Sept 4, 2026 (announced Sept 3). First "Critical" cyber-rated model. Vendor: FrontierMath Tier 4 98%, ARC-AGI-3 99.9%, ExploitBench 100%, OSWorld 2.0 72.6%, Terminal-Bench 4.0 57.9%. Pricing: [developers.openai.com/api/docs/pricing](https://developers.openai.com/api/docs/pricing).
- Note: **GPT-6.1 Sol** (DevDay Sept 29) sits just below Astra at ✅ $2/$10 — the near-flagship value pick; covered in [awesome-flash-llms](https://github.com/dakotac1994/awesome-flash-llms).

### Anthropic

- [Claude Fable 5.1](https://www.anthropic.com/claude-fable-and-mythos-5-1) — ✅ **$10 in / $50 out** (input read live on the pricing card; output per Anthropic's announcement, corroborated by 3 independent write-ups). ~1M in / 128K out; adaptive thinking always on. Released Sept 1, 2026; gated twin **Claude Mythos 5.1** (identical weights, trusted-access only). Vendor: Terminal-Bench 4.0 55.8%, TB-Science 52.6%, GDPval-AA 1853, OSWorld 2.0 77.9% partial, Humanity's Last Exam 60.9%, CursorBench 73.4%. Independent: BenchAlign #1 (84.76), LogRocket coding #1 (1762 Elo). Pricing: [claude.com/pricing#api](https://claude.com/pricing#api).
- Note: **Claude Opus 5.5** (Sept 22, ✅ $4/$20) is Anthropic's recommended "daily driver" — one tier below Fable 5.1.

### Google DeepMind

- [Gemini 3.1 Pro](https://ai.google.dev/gemini-api/docs/models) — ✅ **$2 in / $12 out** (≤200K prompt); **$4/$18** (>200K). 1,048,576 in / 65,536 out; Deep Think reasoning; Batch 50% off. Preview since Feb 19, 2026. Vendor: ARC-AGI-2 77.1%, SWE-Bench Verified 80.6%. Pricing: [ai.google.dev/pricing](https://ai.google.dev/pricing).
- Note: **Gemini 3.5 Pro was announced at I/O (May 19, 2026) but never shipped** as of Sept 29, 2026 (missed June, July 17, and early-Aug targets; partner testing only per Sept 20 reporting).

### xAI

- [Grok 4.7](https://x.ai/news/grok-4-7) — ✅ **$2 in / $6 out** (<200K prompt; cached $0.50); **$4/$12** (≥200K). 500K context; 2.1T params; reasoning effort low→xhigh. Released Sept 21, 2026. Vendor: DeepSWE 71.0% (xHigh), CursorBench 4.0 46.3%, Terminal-Bench 4.0 38.0%, EEBench 64.0%. Independent: AA Intelligence Index 46.45. Pricing: [docs.x.ai/developers/pricing](https://docs.x.ai/developers/pricing) (page dated Sept 29, 2026).
- Note: a 2x-speed "Fast" variant is served at 2x price via Cursor + Grok Build.

### DeepSeek

- [DeepSeek V4 Pro](https://api-docs.deepseek.com/quick_start/pricing) — ⚠️ **$0.66 in / $1.98 out (off-peak); $1.32/$3.96 (peak)**. 1M in / 384K out; 1.6T MoE / 49B active. Peak hours 01:00–04:00 & 06:00–10:00 UTC Mon–Fri. **MIT open weights.** Vendor: SWE-bench Verified >80%, GPQA Diamond 92.4%. Rates effective Aug 16, 2026; the planned Sept 14 sunset was **cancelled** — still served.

### Alibaba — Qwen

- [Qwen3.8-Max](https://help.aliyun.com/en/model-studio/qwen3-8-max) — ⚠️ **$2 in / $6 out** (cached $0.25; Singapore list). 1M context; 2.4T MoE / 95B active; thinking and non-thinking modes. GA Aug 3, 2026 (snapshot `qwen3.8-max-0902`). Code Arena WebDev #1 (1,691, Sept 2026). Open-weights checkpoint (Qwen3.8-2.4T-A95B) under a custom license. Note: **Qwen 4 Max announced Sept 22, 2026 but had no public specs, price, or launch date at cutoff.**

### Zhipu AI — GLM

- [GLM-5.3](https://www.z.ai) — ⚠️ **$1.40 in / $4.40 out** (cached $0.26). ~1M context; ~743B params. API release Aug 18, 2026. **Open weights under a custom (non-permissive) license.** Vendor: +50% coding over GLM-5.2; CyberGym 84.5%.

### Moonshot AI — Kimi

- [Kimi K3](https://www.kimi.com/blog/kimi-k3) — ✅ **$3 in / $15 out** (cached $0.30; stated in the official tech blog; API platform at [platform.kimi.ai](https://platform.kimi.ai/)). 1M context; native vision; 2.8T / ~104B active — the largest open model at release. **Modified MIT open weights.** Released July 16, 2026 (weights July 27). Long-horizon coding; Moonshot's official blog reports DeepSWE 67.3 with the mini-SWE-agent harness.

### MiniMax

- [MiniMax M3](https://platform.minimax.io/docs/guides/pricing-paygo) — ⚠️ **$0.30 in / $1.20 out** (≤512K ctx); **$0.60/$2.40** (>512K). 1M combined context; 428B / 23B active; text/image/audio/video multimodal. **Open weights (MiniMax Community License).** Vendor: SWE-Bench Pro 59.0%, Terminal-Bench 2.1 66.0%. Released June 1, 2026.

### Mistral AI

- [Mistral Large 3](https://docs.mistral.ai/models/mistral-large-3-25-12) — ✅ **$0.50 in / $1.50 out** (Batch −50%; cached input up to −90%). 256K context; 675B MoE / ~41B active; native multimodal. **Apache 2.0 open weights.** EU-native, GDPR-friendly. Released Dec 2, 2025 — still the flagship per multiple Sept-2026 sources. Pricing: [mistral.ai/pricing](https://mistral.ai/pricing/).
- Note: a "Mistral Large 4" (claimed July 2026) is single-sourced and contradicted — **excluded as unconfirmed**.

### Cohere

- [Command A+](https://cohere.com/pricing) — ⚠️ **no public per-token price** (production via Model Vault dedicated deployments or self-hosting; eval API free). 128K in / 64K out; 218B / 24B active; 48 languages. **Apache 2.0 open weights.** Enterprise RAG/knowledge-work focus. (Command A non-plus remains the self-serve default at 256K context.)

### Amazon — Nova

- **Nova 2 Pro** — ⚠️ **pricing unknown** (preview-gated to Nova Forge customers; no public model card or published benchmarks). Amazon's most intelligent model when it goes GA. [aws.amazon.com/ai/generative-ai/nova](https://aws.amazon.com/ai/generative-ai/nova)
- [Nova 2 Lite](https://aws.amazon.com/ai/generative-ai/nova) — ⚠️ **$0.30 in / $2.50 out**. 1M in / 64K out. The current GA Nova flagship-class model on Bedrock.

### Meta

- [Muse Spark 1.3](https://developer.meta.com/ai/resources/blog/build-with-muse-spark/) — ⚠️ **$1.25 in / $4.25 out**. 1M context; image/video/document multimodal. Released Sept 2, 2026 (max-reasoning variant Sept 4). Independent: AA Intelligence Index 62; LiveBench rank 5 at $0.219/task. Meta-ecosystem integration (WhatsApp/Instagram/Workplace). Conflicting "Llama 5" reports are unverified; Llama 4 Maverick remains the open-weight flagship line.

### Baidu — ERNIE

- [ERNIE 5.1](https://intl.cloud.baidu.com/en/doc/qianfan/s/7m95lyy43-intl-en) — ⚠️ **$0.59 in / $2.65 out** (converted from official CNY rates). 128K context. Preview Apr 29, 2026; released May 8, 2026. Independent: LMArena Text 1476 (**#1 China**), LMArena Search 1223 (**#1 China, #4 global**). Served on Baidu Qianfan.

### StepFun

- [step-3.7-flash](https://huggingface.co/stepfun-ai/Step-3.7-Flash-FP8) — ⚠️ **$0.20 in / $1.15 out** (cached $0.04). 256K in / 230,400 max out; 198B MoE / 11B active; multimodal. **Apache 2.0 open weights.** Released May 2026. SWE-Bench PRO 56.3% (2nd place), Terminal-Bench 2.1 59.5%. The cheapest flagship in this survey — the "Flash" name notwithstanding, this is StepFun's most capable model.

### Xiaomi — MiMo

- [MiMo-V2.6-Pro](https://mimo.mi.com) — ⚠️ **$0.435 in / $0.87 out** (cached $0.0036). 1M in / 128K out; omnimodal (text/image/audio/video); 1.02T / 42B active. **MIT open weights.** Released Sept 21, 2026. Independent: AA Intelligence Index 46 — **#1 open-weight** (tied Grok 4.7).

### Microsoft

- **MAI-Thinking-1** — ⚠️ **no per-token list price** (billed via Microsoft Foundry input/output usage meters; [pricing details](https://azure.microsoft.com/pricing/details/microsoft-foundry/)). 256K total per-request budget / 64K output cap; 35B active-param MoE; trained from scratch on commercially licensed data (no-distillation claim). Announced at Build 2026 (June 2); private preview on Foundry. Vendor claims only: preferred over Claude Sonnet 4.6 in blind evals; matches Claude Opus 4.6 on SWE-bench Pro.

### NVIDIA — Nemotron

- [Nemotron 3 Ultra](https://build.nvidia.com) — ⚠️ **no NVIDIA token list price published** (third-party hosts vary). 1M in / 66K out; 550B / 55B active; hybrid Mamba-Transformer MoE. **Open weights (commercial license).** Independent: AA Intelligence Index 47.7. Released June 4, 2026.

### Tencent — Hunyuan

- [Hy4 Preview](https://github.com/tencent-hunyuan/hy4-preview) — ⚠️ **$0.834 in / $2.501 out** (cached $0.042; vendor list via TokenHub price compilation, Sept 2026). >1M context; 770B / 49B active. **Apache 2.0 open weights.** Open-sourced Sept 2026; served via Tencent Cloud TokenHub and OpenRouter. Vendor internal blind eval: 2.99/4.00 over 163 experts / 203 engineering tasks (vs GLM-5.3 2.92, Kimi K3 2.94) — vendor-internal, not independent.
- [Hy3](https://github.com/tencent-hunyuan/hy4-preview) — ⚠️ **$0.15 in / $0.59 out** (converted from official CNY rates). 256K context; 295B / 21B active; hybrid thinking, native tool calling. **Apache 2.0 open weights.** Released July 6, 2026. The stable GA option while Hy4 is in preview. (Weights live under the same official [Tencent-Hunyuan](https://github.com/Tencent-Hunyuan) org.)

### ByteDance — Doubao/Seed

- [Doubao-Seed-2.1 Pro](https://seed.bytedance.com) — ⚠️ **¥6 in / ¥30 out per 1M** (official CNY via third party; USD not converted). ~256K context (unconfirmed). Released June 23, 2026. Vendor claims leadership on Terminal Bench 2.1, SWE-Pro, SciCode, OSWorld, MMMU-Pro — exact scores not published. Closed API.

---

## Open-weight flagships

The flagships you can download and run yourself, as of Sept 2026:

| Model | License | Why it matters |
|---|---|---|
| [DeepSeek V4 Pro](https://api-docs.deepseek.com/quick_start/pricing) | MIT | Cheapest frontier-class reasoning; peak/off-peak billing |
| [Kimi K3](https://www.kimi.com/blog/kimi-k3) | Modified MIT | First 3T-class open model (2.8T / 104B active) |
| [MiMo-V2.6-Pro](https://mimo.mi.com) | MIT | #1 open-weight on AA Index (46); omnimodal |
| [Mistral Large 3](https://docs.mistral.ai/models/mistral-large-3-25-12) | Apache 2.0 | EU-native, GDPR-friendly |
| [step-3.7-flash](https://huggingface.co/stepfun-ai/Step-3.7-Flash-FP8) | Apache 2.0 | Cheapest flagship price in the survey |
| [GLM-5.3](https://www.z.ai) | Custom (non-permissive) | Long-horizon coding; check license before commercial use |
| [MiniMax M3](https://platform.minimax.io/docs/guides/pricing-paygo) | MiniMax Community License | Multimodal 1M context; check license terms |
| [Command A+](https://cohere.com/pricing) | Apache 2.0 | Enterprise RAG; self-host or Model Vault |
| [Nemotron 3 Ultra](https://build.nvidia.com) | Commercial license | Hybrid Mamba-Transformer architecture |
| [Hy4 Preview](https://github.com/tencent-hunyuan/hy4-preview) | Apache 2.0 | 770B; preview-class |
| [Hy3](https://github.com/tencent-hunyuan/hy4-preview) | Apache 2.0 | Stable GA open option |
| [Qwen3.8-Max](https://help.aliyun.com/en/model-studio/qwen3-8-max) | Custom license (Qwen3.8-2.4T-A95B checkpoint) | 2.4T MoE open checkpoint; check terms |

---

## Benchmarks & eval notes

See [docs/benchmarks-notes.md](docs/benchmarks-notes.md) for the full treatment. Key points:

- **Vendor vs independent:** vendor numbers are self-served; treat independent leaderboards (Artificial Analysis Intelligence Index, LMArena, BenchAlign, LiveBench) as the reality check. GPT-6 Astra's vendor OSWorld 2.0 (72.6%) vs Fable 5.1's (77.9% partial / 41.7% strict) shows why same-benchmark cross-vendor comparison needs matching harnesses.
- **The price-performance frontier:** xAI publishes a price/performance chart directly (Grok 4.7: CursorBench 46.3% at $2/$6 vs Fable 5.1 Max at $10/$50 with 51.8%) — the whole point of tracking prices alongside scores.
- **Agentic benchmarks are the 2026 currency:** Terminal-Bench 4.0, OSWorld 2.0, DeepSWE, TB-Science, and GDPval matter more than MMLU-style static evals for flagship comparison.
- **Benchmarks that moved markets in 2026:** Qwen3.8-Max debuted #1 on Code Arena WebDev (1,691); ERNIE 5.1 topped LMArena's China charts; MiMo-V2.6-Pro took #1 open-weight on the AA Index.

## Retired & superseded flagships (2026)

| Model | Fate | Date |
|---|---|---|
| GPT-5.6 Sol | Superseded by GPT-6 Astra (still served; $4/$20 promo through Nov 21, 2026) | Sept 2026 |
| Claude Fable 5 | Superseded by Fable 5.1 (legacy; retirement no sooner than 2027-06-09) | Sept 2026 |
| Claude Opus 5 | Superseded by Opus 5.5 (Sept 22) | Sept 2026 |
| Grok 4.6 | Superseded by Grok 4.7 | Sept 2026 |
| GLM-5 / 5.1 / 5.2 | Superseded by GLM-5.3 | Aug 2026 |
| Kimi K2.5 | Retired | Aug 31, 2026 |
| Qwen3.7 Plus | Superseded by Qwen3.8-Max | Aug 2026 |
| Nova Premier | Legacy / EOL | Sept 14, 2026 |
| Doubao-Seed 2.0 | Superseded by Seed-2.1 Pro | 2026 |
| DeepSeek V4 Pro (planned sunset) | Sunset **cancelled** — still served | Sept 2026 |

Announced but unshipped at cutoff: **Gemini 3.5 Pro** (Google), **Qwen 4 Max** (Alibaba). Full history in [docs/status-changes.md](docs/status-changes.md).

## Guides

- [Choosing a flagship model](docs/choosing-a-flagship-model.md) — decision guide by workload
- [Benchmarks & eval notes](docs/benchmarks-notes.md) — how to read the numbers
- [Glossary](docs/glossary.md) — terms used in this repo
- [Status changes](docs/status-changes.md) — retirements, renames, pricing changes

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). One entry = one model; prices are stamped with their verification date and never guessed.

## License

[MIT](LICENSE) © 2026 dakotac1994
