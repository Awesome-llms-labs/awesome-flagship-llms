# Glossary

Terms used in this repo.

- **Flagship:** the most capable general-purpose model a lab offers. Excludes efficiency tiers (flash/mini/haiku/nano) and specialized models (embedding, moderation, image-only).
- **Efficiency tier:** a lab's cheaper, faster line (e.g. Gemini Flash, GPT-6 Luna, Claude Haiku). Covered in [awesome-flash-llms](https://github.com/dakotac1994/awesome-flash-llms).
- **Open weights:** model weights are downloadable. License varies: MIT/Apache 2.0 (permissive), modified MIT / community / custom (read the terms), commercial (restricted).
- **Closed:** API-only; weights not available.
- **MoE (Mixture of Experts):** architecture that routes each token to a subset of "expert" sub-networks. Reported as total/active params (e.g. 2.8T / 104B active).
- **Context window:** max tokens of input the model can consider at once. "1M" = ~1,000,000 tokens (~750K English words).
- **Cached input:** re-using previously processed prompt tokens at a discount (typically 75–99% off). Dominates cost for agentic workloads with repeated context.
- **Peak/off-peak:** DeepSeek varies prices by time of day (UTC). Off-peak can be 50% cheaper.
- **Reasoning effort:** how much internal "thinking" the model does (low/medium/high/xhigh/max). Higher effort = better scores, more output tokens, higher cost.
- **Preview / gated:** available to limited users only (Nova 2 Pro, MAI-Thinking-1, Hy4 Preview, Claude Mythos 5.1). Pricing often unpublished.
- **EOL (end of life):** the vendor stops serving the model (e.g. Nova Premier, Sept 14, 2026).
- **AA Index:** Artificial Analysis Intelligence Index — an independent composite benchmark score.
- **LMArena:** blind human-preference leaderboard (Elo-style).
- **Unverified (⚠️):** price or fact from a third-party source, not read on the vendor's official page. Never guessed.
- **Verified (✅):** read on the vendor's official pricing page or official announcement, with the read date.
