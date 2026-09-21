# Otniel Gomes

**AI Engineer** — I build and evaluate LLM systems with measurable quality, latency, and observability.

<p align="center">
  <strong>Language:</strong> English | <a href="README.pt-BR.md">Português</a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/otnielgomes/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:otniel.g.andrade@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science"><img src="https://img.shields.io/badge/Case_studies-portfolio-1f425f?style=for-the-badge&logo=github" alt="Portfolio" /></a>
</p>

<p align="center">
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" /></a>
  <a href="https://www.langchain.com/langgraph"><img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangGraph" /></a>
  <a href="https://docs.ragas.io/"><img src="https://img.shields.io/badge/RAGAS-evaluation-6366F1?style=for-the-badge" alt="RAGAS" /></a>
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

### [AI Customer Support Platform](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector)

**Problem:** Answer questions about real orders without hallucinating, and escalate when policy forbids acting.

**Solution:** TechStore Support uses a LangGraph supervisor that routes each ticket to billing, logistics, or account workers. Those workers read order facts from PostgreSQL, retrieve procedures through RAG over pgvector, and run a deterministic policy engine before any refund or cancellation.

**Result:** Customer Portal and Support Console deployed on DigitalOcean App Platform, with OpenTelemetry and Langfuse tracing. Unit and integration suites currently pass **160 tests** at about **70%** coverage. Unauthorized refunds stay blocked in code.

**[Repository](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)**

---

### [AI Agent with Docker, LangGraph & Email](https://github.com/OtnielGomes/AI-Agent-with-Docker-Containers-and-Python)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://streamlit.io/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

**Problem:** Researching a topic, reading the inbox, and sending a reply is slow when it is done by hand every time.

**Solution:** A LangGraph supervisor routes work to a research agent and an email agent (Gmail IMAP/SMTP). FastAPI serves the API, PostgreSQL keeps chat history, Streamlit is the UI — packaged with Docker Compose.

**Result:** Deployed on DigitalOcean App Platform as API, Streamlit UI, and managed PostgreSQL.

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

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

**Retrieval**

[![PostgreSQL](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector) [![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat-square)](https://www.trychroma.com/) [![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/)

**Evaluation & observability**

[![RAGAS](https://img.shields.io/badge/RAGAS-6366F1?style=flat-square)](https://docs.ragas.io/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/) [![Langfuse](https://img.shields.io/badge/Langfuse-F4B942?style=flat-square)](https://langfuse.com/) [![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)](https://opentelemetry.io/) [![Pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://docs.pytest.org/) [![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=astral&logoColor=white)](https://docs.astral.sh/uv/)

Background in modeling and data platforms (PyTorch, scikit-learn, Spark, Databricks) sits behind this work; it is not the focus of this profile.

## Contact

**Otniel Gomes** — AI Engineer · Bauru, SP

- Email: [otniel.g.andrade@gmail.com](mailto:otniel.g.andrade@gmail.com)
- LinkedIn: [linkedin.com/in/otnielgomes](https://www.linkedin.com/in/otnielgomes/)
- GitHub: [@OtnielGomes](https://github.com/OtnielGomes)
- Case studies: [Portifolio--AI-Engineering--Data-Science](https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science)
