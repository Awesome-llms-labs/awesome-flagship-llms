# Benchmarks & eval notes

How to read the benchmark figures cited in this repo (as of September 2026).

## The two kinds of numbers

- **Vendor-reported:** measured by the lab, on its own harness. Useful for capability claims, but harnesses differ (effort level, tooling, sampling) — cross-vendor comparison needs matching setups. Always labeled as vendor.
- **Independent:** third-party leaderboards and evals (Artificial Analysis Intelligence Index, LMArena, BenchAlign, LiveBench, Terminal-Bench public leaderboard). The reality check.

## Benchmarks that matter in 2026

| Benchmark | What it tests | Why it matters |
|---|---|---|
| Terminal-Bench 4.0 / TB-Science | Agentic terminal coding and scientific workflows | The flagship coding benchmark; GPT-6 Astra leads at 57.9% / 64.6% (science) |
| OSWorld 2.0 | Computer-use agents in real OS environments | The computer-use benchmark; note "partial" vs "strict" scoring differ wildly (Fable 5.1: 77.9% partial vs 41.7% strict) |
| DeepSWE | Long-horizon software engineering | Grok 4.7 71.0% (xHigh), Kimi K3 67.3 |
| SWE-bench Verified / PRO | Real GitHub issue resolution | The classic; still the first number vendors quote |
| CursorBench | Longer-running coding tasks | xAI's home turf (Grok 4.7: 46.3%) |
| GDPval / AA Briefcase | Professional knowledge work (lawyers, analysts) | Fable 5.1 GDPval-AA 1853 leads |
| LMArena | Blind human preference | ERNIE 5.1's 1476 text / 1223 search show regional strength |
| AA Intelligence Index | Composite independent index | Single number for cross-model ranking: Fable 5.1's peers sit 46–62 |

## Traps

1. **Harness mismatch:** the same model scores differently under different harnesses (Kimi's blog shows this explicitly for DeepSWE). Compare within one harness.
2. **Effort levels:** reasoning effort (low→max/xhigh) changes scores and cost simultaneously. Vendor SOTA claims are usually at max effort.
3. **"Partial" vs "strict":** OSWorld's partial-credit scoring roughly doubles strict scores — never compare a partial number to a strict one.
4. **Index rebasing:** Artificial Analysis rebases its Intelligence Index (v4.1.1 vs v4.3.2); cross-version comparisons are invalid. Nemotron 3 Ultra's 47.7 (v4.1.1) and MiMo's 46 (v4.3.2) are not directly comparable.
5. **Vendor-internal evals:** Tencent's Hy4 blind eval (2.99/4.00) and Microsoft's MAI-Thinking-1 human-preference claims have no independent reproduction — treat as claims, not standings.
6. **Missing scores:** several flagships (Mistral Large 3, Seed-2.1 Pro, Kimi K3 exact figures) have no citable public numbers. Absence of a score is not evidence of weakness — it's a gap in the record, and this repo marks it as such.

## Versioning

Benchmark figures are tied to the model version and date in the README. When a model updates, its scores may change — check [status-changes.md](status-changes.md).
