<!-- Your phone number becomes public once this repo is public. Delete it from the contact line if you'd rather not list it. -->
<!-- Replace the LinkedIn URL with your own profile link. -->

<div align="center">

# Vennela Kothari

**AI/ML Engineer · GenAI Systems Engineer · LLM Engineer**

Dubai, UAE

[vennelakothari10@gmail.com](mailto:vennelakothari10@gmail.com) · [LinkedIn](https://linkedin.com) · +971 585060560

</div>

---

## About

I build GenAI systems with hard latency and accuracy budgets.

Full-stack background. I own the retrieval layer, the API, and the UI.

**Focus areas:** RAG pipelines · LLM inference optimization · query routing · evaluation and observability

**Open to:** AI/ML Engineer, GenAI Systems Engineer, LLM Engineer

---

## Projects

### 1. AI Cognitive Routing System

Embedding-based complexity router. Modeled on Kahneman's System 1 / System 2 split.

It scores each incoming query. Simple queries take a fast heuristic path. The deep reasoning model runs only when the query needs it.

```text
Query → Embedding → Complexity score ─┬─ low  → Fast heuristic path
                                      └─ high → Deep reasoning model

Logging: latency · cost per query · P95 → threshold tuning
```

| Metric | Result |
|---|---|
| Routing accuracy | **87%** on live inference logs |
| Observability | Real-time latency, cost per query, P95 response time |
| Threshold tuning | Driven by logged metrics, automated |

**Stack:** Python · FastAPI · Streamlit · NLP embeddings · Logging

---

### 2. Production-Grade RAG System

Stateless, async, two-stage dense retrieval pipeline. Built for internal enterprise policy extraction.

```text
Query → FAISS dense retrieval → Cross-encoder rerank → Context check ─┬─ pass → LLM answer
                                                                      └─ fail → NO CONTEXT
```

**Design choices**
- FAISS handles recall. The cross-encoder handles precision.
- Stateless, async services. No session state held in the API layer.
- Strict **NO CONTEXT** fallback. Out-of-corpus queries get a refusal, not a guess.

| Metric | Result |
|---|---|
| Faithfulness | **0.85+** on a custom evaluation suite |
| End-to-end latency | **Under 300 ms**, front end to back end |
| Out-of-corpus queries | Handled by the NO CONTEXT fallback, no generated answer |

**Stack:** Python · FastAPI · FAISS · Cross-encoder reranking · PostgreSQL · React · Node

---

## Technical Toolkit

| Area | Tools |
|---|---|
| **Languages** | Python, SQL, JavaScript, Java, C |
| **ML Frameworks & Libraries** | FAISS, Transformers, TensorFlow, PyTorch, Keras, Scikit-learn, LangChain, LlamaIndex |
| **Backend & Databases** | FastAPI, Node.js, Express, PostgreSQL, MySQL, MongoDB, Redis, React JS |
| **MLOps & Infrastructure** | AWS Fundamentals (EC2, S3), Git, GitHub, Docker, Postman, MLflow, CI/CD for ML |

---

## Contact

- Email: [vennelakothari10@gmail.com](mailto:vennelakothari10@gmail.com)
- LinkedIn: [linkedin.com](https://linkedin.com)
- Phone: +971 585060560
- Location: Dubai, UAE
