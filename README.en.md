# amber-nous

Benchmarking models sold on **Nous Portal** (inference-api.nousresearch.com) against the private **AMBER** suite — results only, never the questions.
中文: [README.md](README.md)

## What this is

- One `results/YYYY-Www.md` per period: same questions, same harness, full-library runs; same-named models compared across vendors.
- Each report pins: suite size and hashes, per-case d2 scores and pass/fail, terminal states, token usage and cost (pay-as-you-go lane, real prices), latency, environment fingerprints, and qualitative verdicts written under evidence discipline.
- Questions, oracles, transcripts, and intermediate artifacts are **never published** (see "Publication rules").
- Sibling repos: [amber-commandcode](https://github.com/getaskclaw/amber-commandcode), [amber-opencode](https://github.com/getaskclaw/amber-opencode), [amber-deepseek](https://github.com/getaskclaw/amber-deepseek), [amber-gpt](https://github.com/getaskclaw/amber-gpt), [amber-crof](https://github.com/getaskclaw/amber-crof), [amber-ollama](https://github.com/getaskclaw/amber-ollama), [amber-devin](https://github.com/getaskclaw/amber-devin). The comparison axis here is **same model name, different vendor lanes** — a model name on Nous Portal / CommandCode / xAI official may be a different endpoint; cross-repo references always carry date and effort-band declarations.
- AMBER is an agentic, real-work suite (build / ops / review / vision / requirement-drift). Spec and tooling: [getaskclaw/amber](https://github.com/getaskclaw/amber); the question bodies stay private.

## Publication rules (hard lines)

1. Publish only: scores and aggregates, token usage and cost, speed, qualitative verdicts.
2. Never publish: question content, oracles/graders, transcripts, candidate workspaces, or any intermediate artifact that could reconstruct a question.
3. Every issue pins: model ID, effort band, date (UTC), harness version, per-case content hash (bundle_sha), cross-checked against the public hash index in [amber](https://github.com/getaskclaw/amber).
4. Case numbers and suite structure are private: public results use stable aliases (A-xxxxxxxx, hash-derived) plus bundle hashes only; internal case IDs, variant names, and question descriptions never appear.
5. Tone: this is community measurement, not an attack on vendors. Data talks; wording stays restrained.
