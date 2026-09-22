# amber-nous

Benchmarking models sold on **Nous Portal** (inference-api.nousresearch.com) against the private **AMBER** suite — results only, never the questions.
中文: [README.md](README.md)

> **In one line**: we hand AI models real work — fix a bug, find a root cause, review a system screenshot, operate a live system — and this repo holds the report cards for models sold on **Nous Portal**. Latest issue: Grok 4.7 passed 13 of 24 tasks, is the family's best root-cause detective, and on 7 tasks it wrote one line of plan and handed in the page.

## What this is

- One `results/YYYY-Www.md` per period: same questions, same harness (the program that runs the exam and scores it), full-library runs; same-named models compared across vendors.
- Each report pins: suite size and hashes (a hash is the fingerprint that proves questions were not swapped), per-case d2 scores (our own scoring; the algorithm stays private) and pass/fail, terminal states, token usage and cost (real prices on pay-as-you-go lanes), latency, environment fingerprints, and qualitative verdicts written under evidence discipline.
- Questions, oracles (the graders), transcripts (full answer logs), and intermediate artifacts are **never published** (see "Publication rules").
- AMBER is an agentic, real-work suite (build / ops / review / vision / requirement-drift — the requirements change mid-task). Spec and tooling: [getaskclaw/amber](https://github.com/getaskclaw/amber); the question bodies stay private.
- A "lane" is one vendor's shop/API for a model name (e.g. the CommandCode lane, the Nous Portal lane); "effort band" is the thinking-effort setting we give the model. The same model name on different lanes may be a different endpoint, so cross-repo references always carry date and band declarations.

## Sibling repos

[amber-commandcode](https://github.com/getaskclaw/amber-commandcode) · [amber-opencode](https://github.com/getaskclaw/amber-opencode) · [amber-deepseek](https://github.com/getaskclaw/amber-deepseek) · [amber-gpt](https://github.com/getaskclaw/amber-gpt) · [amber-crof](https://github.com/getaskclaw/amber-crof) · [amber-ollama](https://github.com/getaskclaw/amber-ollama) · [amber-devin](https://github.com/getaskclaw/amber-devin)


## Latest results

- **2026-W39** — x-ai/grok-4.7 first full-library run, 13/24: [full report](results/2026-W39.en.md)（[中文](results/2026-W39.md)）· [explainer with chart](docs/explainers/2026-W39-g47-plain.en.md)（[中文](docs/explainers/2026-W39-g47-plain.md)）

![Win rate per axis](results/assets/2026-W39-axes.en.png)


## Publication rules (hard lines)

1. Publish only: scores and aggregates, token usage and cost, speed, qualitative verdicts.
2. Never publish: question content, oracles/graders, transcripts, candidate workspaces, or any intermediate artifact that could reconstruct a question.
3. Every issue pins: model ID, effort band, date (UTC), harness version, per-case content hash (bundle_sha), cross-checked against the public hash index in [amber](https://github.com/getaskclaw/amber).
4. Case numbers and suite structure are private: public results use stable aliases (A-xxxxxxxx, hash-derived) plus bundle hashes only; internal case IDs, variant names, and question descriptions never appear.
5. Tone: this is community measurement, not an attack on vendors. Data talks; wording stays restrained.
