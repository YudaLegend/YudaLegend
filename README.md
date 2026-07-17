# Haonan Jin

**AI Engineer · MSc Data Science (UPC Barcelona)** — I build LLM systems that run in production, and I measure them.

📍 Barcelona · 📧 [a779052016@gmail.com](mailto:a779052016@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/YOUR-LINKEDIN-HERE) · 🎯 Open to AI Engineer / Data Scientist roles

---

## What I've built

### 🤖 [TaskFlow Support Agent](https://github.com/YudaLegend/taskflow-support-agent) — production LLM agent, live demo
A customer-support agent built the way production systems should be: **LangGraph ReAct** loop with typed tools, RAG over ChromaDB, guardrails against prompt injection, PII redaction, **FastAPI + SSE** streaming API.
- **Observability**: Langfuse traces per request (tokens, latency, cost); user feedback flows back as trace scores
- **Evals, not vibes**: 15 deterministic trajectory scenarios, 25-question retrieval benchmark, A/B backend comparison (Groq vs DeepSeek — 14/15 vs 12/15, 2.2× faster), and one documented negative result (hybrid BM25+dense didn't help — kept the data, dropped the feature)
- **Ships properly**: multi-stage Docker, docker-compose (8 services), GitHub Actions CI (lint + 33 tests), deployed on HuggingFace Spaces

`LangGraph` `ChromaDB` `FastAPI` `MongoDB` `Langfuse` `Docker` `CI/CD`

### 🏥 [Meditab](https://github.com/YudaLegend/meditab) — LLM clinical extraction (master's thesis, 9/10)
Built with **Hospital Clínic de Barcelona**: converts unstructured Catalan psychiatric notes into structured medication histories.
- Pydantic schemas with cross-field invariants that intercept semantically invalid outputs
- Multi-provider inference layer (Gemini, Groq, Ollama → AWS Bedrock in ~30 lines of config)
- Field-level evaluation framework (LLM-as-judge + ROUGE): **macro-F1 0.935**; 150-run experiment matrix across 5 models on 10 real patient histories
- Developed synthetic-first for **GDPR** compliance, deployed in the hospital's secure AWS environment

`Pydantic` `MCP` `AWS Bedrock` `Ollama` `LLM evaluation`

### 🎮 [Context-Aware Toxicity Detection](https://github.com/YudaLegend/Data-Mining-Final) — BERT beyond the black box
Same word, different meaning: "camper" is an insult in FPS, neutral in MOBA. Solved with **learnable soft-prompt embeddings** encoding game genre as context.
- 70k dual-source samples + ~1,000 hand-built adversarial contrastive pairs to break keyword shortcuts
- Interpretability: token-swap sensitivity tests (does the prediction flip when context changes?) + t-SNE embedding visualization
- **92–94% accuracy** with two-phase freeze-unfreeze training on a single RTX 3060

`PyTorch` `HuggingFace Transformers` `fine-tuning` `interpretability`

### ⚡ [Lakehouse Pipeline](https://github.com/brunabarraquer/BDM) — batch + streaming data platform
3-tier **Delta Lake** with full versioning; PySpark batch transforms orchestrated by Airflow (cold path), **Kafka** real-time ingestion driving live leaderboards (hot path), Great Expectations quality gates quarantining bad batches, collaborative-filtering recommender on top.

`PySpark` `Kafka` `Airflow` `Delta Lake` `Great Expectations` `Streamlit`

### 🌐 [kbin](https://github.com/YudaLegend/kbin) — full-stack platform (team of 4, agile)
Reddit-style content aggregator: **Django REST** API (OpenAPI spec, OAuth, S3 media) + **React** SPA. Deployed on Fly.io + Vercel.

`Django` `DRF` `React` `AWS S3`

### 📊 More
- [Steam Games ML pipeline](https://github.com/hangui11/Steam-Games-Satisfaction) — end-to-end over 150k+ games: zone architecture, data quality, CV + hyperparameter tuning, per-module unit tests
- [Multivariate analysis in R](https://github.com/hangui11/League-of-Legends-Analysis) — PCA, MDS, MCA, clustering, discriminant analysis (FactoMineR)

---

## Background

- 🎓 **MSc Data Science** — UPC Barcelona (2024–2026) · GPA 8/10, thesis 9/10 · exchange semester at **Beihang University**, Beijing (GPA 3.77/4)
- 🎓 **BSc Computer Science** — UPC Barcelona (2020–2024)
- 💼 **AI Software Engineer intern** @ Colbai Advisors — private RAG ingestion pipelines on Azure for healthcare-compliance clients
- 🗣️ Spanish, Catalan, Chinese (native) · English (fluent)

## How I work

Every model I ship comes with an evaluation harness. Every service comes with traces. I'd rather document a negative result than ship an unmeasured improvement.

**Stack:** Python · SQL · C++ · PyTorch · LangGraph/LangChain · FastAPI · Spark · Kafka · Airflow · Docker · GitHub Actions · AWS · Azure
