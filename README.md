<div align="center">

# Nishika Yadav

**Backend & AI Engineer** — building the infrastructure that makes LLMs actually work in production

[![LinkedIn](https://img.shields.io/badge/LinkedIn-nishika--yadav-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/nishika-yadav)
[![HuggingFace](https://img.shields.io/badge/🤗_HuggingFace-Nishika26-FFD21E?style=flat)](https://huggingface.co/Nishika26)
[![GitHub](https://img.shields.io/badge/GitHub-nishika26-181717?style=flat&logo=github)](https://github.com/nishika26)
[![Blog](https://img.shields.io/badge/Blog-Tech4Dev-2E8B57?style=flat&logo=rss)](https://projecttech4dev.org/blogs/)

</div>

---

I care about the unsexy parts of AI engineering — the retry logic, the rate limiters, the schema decisions that will haunt you six months later. I've spent the last year and a half building production LLM infrastructure at [Tech4Dev](https://projecttech4dev.org), where the users are NGOs doing real work and the systems actually need to hold.

---

## What I've Built

### 🔧 Kaapi — Multi-Provider LLM Platform
*Backend & AI Engineer | Tech4Dev | Sept 2024 – Present*

A production LLM platform serving NGO clients, built from scratch. Here's what I actually worked on:

- **Multi-provider LLM gateway** across OpenAI, AWS Bedrock, and Gemini — provider-agnostic abstraction in FastAPI + SQLModel that cut new model integration time from days to under 2 hours
- **Document pipeline**: PDF → Markdown → vector store, with chunking, embedding, and OpenAI vector store integration; concurrent uploads via Celery workers + Redis task queuing. Also provisioned a knowledge base on AWS Bedrock + OpenSearch + S3 + IAM so NGO clients can query private document stores without touching infrastructure
- **Guardrails microservice** — separate FastAPI service with validator autodiscovery, A/B testing support, and service-to-service auth. New validators plug in without touching the core platform
- **Fine-tuning & evaluation APIs** — stratified data splits, background job tracking, JSONL preprocessing for OpenAI models; cut manual evaluation effort by ~60%
- **Platform hardening** — SlowAPI + Redis/in-memory hybrid rate limiting, SSRF-protected webhook callbacks
- **LLMOps frontend** — contributed to a Next.js 16 + React 19 + TypeScript frontend including guardrails config UI, document management with upload progress, knowledge base creation, and speech-to-text evaluation
- **Wrote about it**: [Kaapi Guardrails: A Tattle-Tech4Dev Collaboration](https://projecttech4dev.org/kaapi-guardrails-tattle-tech4dev/) · [Sprint reflections on building steadily](https://projecttech4dev.org/ai-platform-building-steadily-khopoli-sprint-reflections/) · [Notes from a two-week sprint](https://projecttech4dev.org/a-crack-in-the-routine-worth-having-notes-from-a-two-week-sprint/)

### 📊 Dalgo — Data Pipelines for NGOs
*Data Engineer | Tech4Dev*

- Built DBT transformation pipelines converting raw NGO field data into analytics-ready models powering dashboards for the Jal Jeevan Mission
- Delivered Apache Superset dashboards that replaced manual reporting for programme teams

### 💬 Natural Language → SQL Chatbot
*AI Engineering Intern | Calfus Inc. | Feb – Aug 2024*

- Production chatbot (Ollama + LlamaIndex + LangChain) letting customers query their cash flow database in natural language, directly integrated with PostgreSQL
- Fine-tuned Llama 2 and CodeLlama for Text-to-SQL using SFTTrainer, ORPOTrainer, DPOTrainer; explored QLoRA 4-bit quantization (GGUF/GPTQ) to run 7B models on constrained hardware

---

## Projects

### 🦙 [Llama 2 Fine-Tuning with QLoRA](https://github.com/nishika26/finetuning_llama2)
Fine-tuned Llama 2-7B on a free Colab T4 GPU using 4-bit QLoRA, cutting VRAM footprint by ~75% with no meaningful accuracy loss. Model variants published on [Hugging Face](https://huggingface.co/Nishika26).

---

## Stack

```
LLM / AI        LangChain · LlamaIndex · LangGraph · Langfuse · Transformers
                Fine-tuning: SFT · ORPO · DPO · QLoRA · RLHF
                RAG · Vector stores · Prompt engineering · Agentic AI · MCP Servers

Backend         FastAPI · SQLModel · SQLAlchemy · Pydantic · Alembic
                Celery · Redis · PostgreSQL · Async Python · Pytest

Cloud & Infra   AWS (Bedrock · S3 · IAM · OpenSearch) · Docker · GitHub Actions

ML / Data       PyTorch · TensorFlow · Keras · Scikit-learn · DBT · Apache Superset

LLM Providers   OpenAI · Anthropic · AWS Bedrock · Gemini · Ollama · Hugging Face

Languages       Python · SQL · C++ · TypeScript (working knowledge)
```

---

## What I Want to Work On Next

I'm most excited about problems at the intersection of **reliability and intelligence** — the places where making AI systems actually trustworthy requires both systems thinking and ML depth.

**Specifically:**

- **LLM infrastructure at scale** — multi-tenant serving, cost-aware routing, latency optimization across providers. I've built single-tenant versions of these; I want to work on the harder multi-tenant, high-QPS versions
- **RAG that actually works** — not demos, but production RAG where retrieval quality is measurable, chunk strategies are principled, and evaluation is automated. I want to work on the evaluation and iteration loop more deeply
- **Agentic systems with real reliability guarantees** — checkpointing, rollback, human-in-the-loop at the right moments. I've built async pipelines; I want to push into agents that are genuinely trustworthy
- **Fine-tuning pipelines end-to-end** — I've done QLoRA experiments and built fine-tuning APIs; I want to go deeper into RLHF, preference data collection, and systematic evaluation
- **AI for social impact** — I spent a year building for NGO clients and care about this deeply. Tools that actually get used by field workers, not just pilots that die in staging

---

## Writing

I try to write about what I actually built, not what I wish I'd built.

- [Kaapi Guardrails: A Tattle-Tech4Dev Collaboration for AI Safety](https://projecttech4dev.org/kaapi-guardrails-tattle-tech4dev/)
- [AI Platform Building Steadily: Khopoli Sprint Reflections](https://projecttech4dev.org/ai-platform-building-steadily-khopoli-sprint-reflections/)
- [A Crack in the Routine Worth Having: Notes from a Two-Week Sprint](https://projecttech4dev.org/a-crack-in-the-routine-worth-having-notes-from-a-two-week-sprint/)

---

## Background

B.E. Electrical Engineering, MITS Gwalior (2024) — got into ML through speech separation research at IIIT, then never looked back. Certified in Neo4j & LLM Fundamentals. Volunteer at [People+AI](https://people-plus-ai.in/).

---

<div align="center">

*Open to backend/AI engineering roles — hybrid Bangalore or remote. If you're building something real, let's talk.*

**nishikayadav26@gmail.com**

</div>
