# Otniel Gomes

**AI Engineer** — I build and evaluate LLM systems for measurable quality, latency, and observability, with LangChain, LangGraph, and LangSmith, in Python and TypeScript, on PostgreSQL, Docker, and OpenAI.

<p align="center">
  <strong>Language:</strong> English | <a href="README.pt-BR.md">Português</a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/otnielgomes/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:otniel.g.andrade@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science"><img src="https://img.shields.io/badge/Case_studies-portfolio-1f425f?style=for-the-badge&logo=github" alt="Portfolio" /></a>
</p>

<p align="center">
  <a href="https://www.langchain.com/"><img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" /></a>
  <a href="https://www.langchain.com/langgraph"><img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangGraph" /></a>
  <a href="https://smith.langchain.com/"><img src="https://img.shields.io/badge/LangSmith-FF6B35?style=for-the-badge" alt="LangSmith" /></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" /></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /></a>
  <a href="https://www.postgresql.org/"><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" /></a>
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" /></a>
  <a href="https://openai.com/"><img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI" /></a>
</p>

<p align="center">
  <a href="https://ollama.com/"><img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" /></a>
  <a href="https://github.com/features/actions"><img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" /></a>
  <a href="https://nextjs.org/"><img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" /></a>
  <a href="https://developer.mozilla.org/docs/Web/JavaScript"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" /></a>
</p>

## About

I design LLM-powered systems so the interesting claims can be checked: retrieval quality, policy compliance, and latency — not only a demo chat. Business rules live in **code**; prompts handle language and reasoning, not enforcement.

Currently at [RD Saúde](https://rd.com.br/). Open to **AI Engineering**, **LLM systems**, and applied Generative AI roles.

> [!TIP]
> Architecture diagrams, screenshots, and longer write-ups live in the [case-study portfolio](https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science). This profile is the index.

## How I work

| Practice | What it means in a system |
|---|---|
| **Evaluation before intuition** | Compare prompting and retrieval with RAGAS, BLEU/ROUGE, and LLM-as-Judge instead of picking a stack by feel. |
| **Observability** | Trace every LLM and tool call (LangSmith, Langfuse, OpenTelemetry) so quality and latency are inspectable. |
| **Code vs LLM boundary** | Policy engines, schemas, and databases own refunds, windows, and order facts. The model does not invent state. |
| **Retrieval as a measured pipeline** | Naive, HyDE, and reranking are compared on the same corpus — extra hops have to earn their cost. |
| **Graphs when the problem needs them** | LangGraph for state, tools, escalation, and human-in-the-loop. Complexity follows the problem, not the framework. |
| **Grounded answers or none** | A deterministic citation gate drops citations the corpus cannot support. The answer becomes an explicit refusal instead of a confident paraphrase. |

## Featured work

### [NFe Document Extraction](https://github.com/OtnielGomes/NFe-Document-Extraction)

[![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/) [![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)](https://openai.com/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

**Problem:** A DANFE arrives as a PDF or a phone photo, and accounting still types the fields in by hand.

**Solution:** Header and line-item agents extract the invoice; a deterministic validator, one repair attempt, and human review accept or hold each field.

**Result:** Cheap vision with `gpt-6-luna` scores **0.9870** field accuracy on digital PDFs at **US$ 0.002035** per invoice, and **0.6420** on simulated photos. Planted-error detection is **1.0000** on both.

**[Repository](https://github.com/OtnielGomes/NFe-Document-Extraction)**

---

### [AI Customer Support Platform](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector)

**Problem:** Answer questions about real orders without hallucinating, and escalate when policy forbids acting.

**Solution:** TechStore Support uses a LangGraph supervisor that routes each ticket to billing, logistics, or account workers. Those workers read order facts from PostgreSQL, retrieve procedures through RAG over pgvector, and run a deterministic policy engine before any refund or cancellation.

**Result:** Customer Portal and Support Console deployed on DigitalOcean App Platform, with OpenTelemetry and Langfuse tracing. Unit and integration suites currently pass **160 tests** at about **70%** coverage. Unauthorized refunds stay blocked in code.

**[Repository](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)**

---

### [AI Agent with Docker, LangGraph & Email](https://github.com/OtnielGomes/AI-Agent-with-Docker-Containers-and-Python)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

**Problem:** Reading the inbox and replying by hand is slow, and the assistant must not be the one that hits send.

**Solution:** A LangGraph supervisor routes each message to a research agent (subject and plain-text body) or an email agent (Gmail IMAP, summaries, and drafts). The Next.js UI shows the inbox and a review card: subject, body, and recipient can be edited, and a follow-up updates that same card. FastAPI stores messages and drafts in PostgreSQL. SMTP runs only on Confirm send.

**Result:** Deployed on DigitalOcean App Platform as API, Next.js UI, and managed PostgreSQL. Discarding a draft never touches SMTP.

**[Repository](https://github.com/OtnielGomes/AI-Agent-with-Docker-Containers-and-Python)**

---

### [PGD Teletrabalho](https://github.com/OtnielGomes/Enterprise-Knowledge---RAG-Platform)

[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

**Problem:** A servidor asking about telework rules needs the act actually in force, with an article they can open — not a confident paraphrase.

**Solution:** Ask retrieves Articles from a dated snapshot of five normative acts, drafts an answer, then a deterministic citation gate keeps only citations whose article was retrieved. Unsupported questions return Insufficient Evidence. Current and historical acts are separated; amendments are never silently consolidated.

**Result:** **89** pytest passed with the extractive draft and an empty API key, including a human-annotated golden set of **43** items. Corpus cutoff: **18 September 2026**. CI runs the same golden set on every push.

**[Repository](https://github.com/OtnielGomes/Enterprise-Knowledge---RAG-Platform)**

---

### [LLM-Eval-Suite](https://github.com/OtnielGomes/LLM-Eval-Suite)

[![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)](https://ollama.com/) [![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat-square)](https://www.trychroma.com/) [![RAGAS](https://img.shields.io/badge/RAGAS-6366F1?style=flat-square)](https://docs.ragas.io/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/)

**Problem:** Prompting and RAG strategies are often chosen by intuition, then defended after the fact.

**Solution:** A benchmark that compares Zero-Shot, Few-Shot, and Chain-of-Thought against Naive, HyDE, and reranking retrieval, scored with BLEU, ROUGE, LLM-as-Judge, and RAGAS. Hybrid inference: Ollama Cloud for generation and judging, local embeddings, ChromaDB, traces in LangSmith.

**Result:** Best composite RAGAS **0.988** with HyDE on Gemma3 27B. Best prompting mean accuracy **89.3%** with Qwen3-Coder 480B. Naive RAG stayed competitive on cost; HyDE collapsed on the weakest model.

**[Repository](https://github.com/OtnielGomes/LLM-Eval-Suite)**

---

## Stack

**Orchestration & serving**

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/) [![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)](https://openai.com/) [![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)](https://ollama.com/) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

**Retrieval**

[![PostgreSQL](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector) [![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat-square)](https://www.trychroma.com/) [![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/)

**Interface**

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/docs/Web/JavaScript)

**Evaluation & observability**

[![RAGAS](https://img.shields.io/badge/RAGAS-6366F1?style=flat-square)](https://docs.ragas.io/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/) [![Langfuse](https://img.shields.io/badge/Langfuse-F4B942?style=flat-square)](https://langfuse.com/) [![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)](https://opentelemetry.io/) [![Pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://docs.pytest.org/) [![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=astral&logoColor=white)](https://docs.astral.sh/uv/)

Background in modeling and data platforms (PyTorch, scikit-learn, Spark, Databricks) sits behind this work; it is not the focus of this profile.

## Contact

**Otniel Gomes** — AI Engineer · Bauru, SP

- Email: [otniel.g.andrade@gmail.com](mailto:otniel.g.andrade@gmail.com)
- LinkedIn: [linkedin.com/in/otnielgomes](https://www.linkedin.com/in/otnielgomes/)
- GitHub: [@OtnielGomes](https://github.com/OtnielGomes)
- Case studies: [Portifolio--AI-Engineering--Data-Science](https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science)
