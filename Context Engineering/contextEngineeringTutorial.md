# Context Engineering Workshop

**Retrieval strategies for legal text, from prompt-stuffing to HPC-scale RAG.**

This notebook is a hands-on walkthrough from the DS/AI Collective Cape Town workshop. It teaches when different context and memory strategies fail or succeed, using South African Supreme Court of Appeal judgements as the knowledge source — a legally meaningful corpus the LLM has not been trained on in full detail.

## What it covers

| Section | What happens |
|---------|-------------|
| Prerequisites | DataSpires + Gemini API key setup |
| Part A.1-2 | Load ZASCA-sum dataset, prepare a single-judgement corpus |
| Part A.3 | Strategy 1 — Brute force context stuffing |
| Part A.4 | Strategy 2 — Keyword RAG (cheap, brittle to paraphrase) |
| Part A.5 | Strategy 3 — Semantic RAG with embeddings |
| Part A.6 | Strategy 4 — Hybrid RAG with AI re-ranking |
| Part A.7 | Tricky question probes — paraphrase traps, multi-hop, negation |
| Part B.1-4 | Scale to all 1 000 judgements: ingest, chunk, build corpus DataFrame |
| Part B.5 | HPC embedding job via `client.train()` on the AfriLink cluster |
| Part B.6-9 | FAISS index, semantic search with metadata scoping, full RAG |
| Part B.10-11 | Legal query probes and an experiments dashboard for tuning |
| Part B.12 | Apply the same pipeline to other South African open datasets |

## Dataset

[ZASCA Summarisation](https://huggingface.co/datasets/dsfsi/zasca-sum) — South African Supreme Court of Appeal judgements paired with human-written media summaries. Precise, jurisdictionally relevant, and complex enough to expose where retrieval strategies break.

## Requirements

- **Part A**: A free [Gemini API key](https://aistudio.google.com/app/apikey) — runs entirely in the notebook, no GPU needed
- **Part B**: A [DataSpires](https://dataspires.com) account and `pip install afrilink-sdk` for the HPC embedding job
