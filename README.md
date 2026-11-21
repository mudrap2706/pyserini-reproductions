# Pyserini Reproductions — Mudra Pandya

Pyserini 2.4.0 (commit `f3e502b`) · macOS · 2026-11-20

| Collection | Setup | Metric | Mine | Reference |
|---|---|---|---|---|
| MS MARCO passage (dev) | BM25 tuned, k1=0.82 b=0.68, own index (8,841,823 passages) | MRR@10 | 0.1874 | 0.1874 |
| | | MAP | 0.1958 | 0.1958 |
| | | Recall@1000 | 0.8573 | 0.8573 |
| BEIR NFCorpus (test) | BM25 flat, prebuilt index | nDCG@10 | 0.3218 | 0.3218 |
| | BM25 flat, own index from raw data (3,633 docs) | nDCG@10 | 0.3218 | 0.3218 |
| | | Recall@100 | 0.2457 | 0.2457 |

**Note:** the UKP BEIR server was unreachable, so I pulled NFCorpus from the BeIR Hugging Face mirror, converted it to Pyserini JsonCollection format (title + text), and indexed it myself. Raw evaluation outputs are in `results/`.
