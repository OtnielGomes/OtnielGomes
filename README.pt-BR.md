# Otniel Gomes

**AI Engineer** — eu construo e avalio sistemas com LLM com qualidade, latência e observabilidade mensuráveis.

<p align="center">
  <strong>Idioma:</strong> <a href="README.md">English</a> | Português
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/otnielgomes/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:otniel.g.andrade@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science"><img src="https://img.shields.io/badge/Estudos_de_caso-portfólio-1f425f?style=for-the-badge&logo=github" alt="Portfólio" /></a>
</p>

<p align="center">
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" /></a>
  <a href="https://www.langchain.com/langgraph"><img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangGraph" /></a>
  <a href="https://docs.ragas.io/"><img src="https://img.shields.io/badge/RAGAS-evaluation-6366F1?style=for-the-badge" alt="RAGAS" /></a>
</p>

## Sobre

Eu desenho sistemas com LLM para que as afirmações importantes possam ser checadas: qualidade da recuperação, cumprimento de política e latência — não só um chat de demonstração. Regras de negócio ficam no **código**; prompts guiam linguagem e raciocínio, não a aplicação das regras.

Atualmente na [RD Saúde](https://rd.com.br/). Aberto a papéis de **AI Engineering**, **sistemas com LLM** e Generative AI aplicada.

> [!TIP]
> Diagramas, screenshots e textos longos ficam no [portfólio de estudos de caso](https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science). Este perfil é o índice.

## Como eu trabalho

| Prática | O que isso significa no sistema |
|---|---|
| **Avaliação antes da intuição** | Comparar prompting e recuperação com RAGAS, BLEU/ROUGE e LLM-as-Judge, em vez de escolher o stack no feeling. |
| **Observabilidade** | Rastrear cada chamada de LLM e de ferramenta (LangSmith, Langfuse, OpenTelemetry) para inspecionar qualidade e latência. |
| **Fronteira código vs LLM** | Motores de política, schemas e bancos donos de reembolsos, prazos e fatos do pedido. O modelo não inventa estado. |
| **Recuperação como pipeline medido** | Naive, HyDE e reranking comparados no mesmo corpus — hops extras precisam justificar o custo. |
| **Grafos quando o problema pede** | LangGraph para estado, ferramentas, escalação e human-in-the-loop. Complexidade segue o problema, não o framework. |
| **Resposta ancorada ou nenhuma** | Um gate de citação determinístico descarta o que o corpus não sustenta. A resposta vira uma recusa explícita, em vez de uma paráfrase confiante. |

## Trabalho em destaque

### [AI Customer Support Platform](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector)

**Problema:** Responder sobre pedidos reais sem alucinar, e escalar quando a política impede agir.

**Solução:** O TechStore Support usa um supervisor LangGraph que encaminha cada ticket para agentes de billing, logística ou conta. Esses agentes leem fatos do pedido no PostgreSQL, recuperam procedimentos via RAG em pgvector e passam por um motor de política determinístico antes de qualquer reembolso ou cancelamento.

**Resultado:** Portal do cliente e console de suporte no DigitalOcean App Platform, com traces em OpenTelemetry e Langfuse. Suítes unitárias e de integração passam **160 testes** com cerca de **70%** de cobertura. Reembolsos fora da política ficam bloqueados no código.

**[Repositório](https://github.com/OtnielGomes/AI-Customer-Support-Platform-With-Langgraph)**

---

### [AI Agent with Docker, LangGraph & Email](https://github.com/OtnielGomes/AI-Agent-with-Docker-Containers-and-Python)

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://streamlit.io/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

**Problema:** Pesquisar um tema, ler a caixa de entrada e enviar a resposta é lento quando isso é feito à mão toda vez.

**Solução:** Um supervisor LangGraph distribui o trabalho entre um agente de pesquisa e um agente de e-mail (Gmail IMAP/SMTP). FastAPI serve a API, PostgreSQL guarda o histórico, Streamlit é a interface — empacotado com Docker Compose.

**Resultado:** Publicado no DigitalOcean App Platform como API, UI Streamlit e PostgreSQL gerenciado.

**[Repositório](https://github.com/OtnielGomes/AI-Agent-with-Docker-Containers-and-Python)**

---

### [PGD Teletrabalho](https://github.com/OtnielGomes/Enterprise-Knowledge---RAG-Platform)

[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

**Problema:** Um servidor que pergunta sobre regras de teletrabalho precisa do ato que está de fato em vigor, com um artigo que ele possa abrir — não uma paráfrase confiante.

**Solução:** O Ask recupera artigos de um snapshot datado de cinco atos normativos, redige a resposta e passa por um gate de citação determinístico que só mantém citações cujo artigo foi recuperado. Perguntas sem suporte voltam como Evidência Insuficiente. Atos vigentes e históricos ficam separados; emendas nunca são consolidadas em silêncio.

**Resultado:** **89** testes pytest passando com o rascunho extrativo e chave de API vazia, incluindo um golden set anotado por humano com **43** itens. Corte do corpus: **18 de setembro de 2026**. A CI roda o mesmo golden set a cada push.

**[Repositório](https://github.com/OtnielGomes/Enterprise-Knowledge---RAG-Platform)**

---

### [LLM-Eval-Suite](https://github.com/OtnielGomes/LLM-Eval-Suite)

[![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)](https://ollama.com/) [![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat-square)](https://www.trychroma.com/) [![RAGAS](https://img.shields.io/badge/RAGAS-6366F1?style=flat-square)](https://docs.ragas.io/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/)

**Problema:** Estratégias de prompting e RAG costumam ser escolhidas por intuição e justificadas depois.

**Solução:** Um benchmark que compara Zero-Shot, Few-Shot e Chain-of-Thought com recuperação Naive, HyDE e reranking, pontuado com BLEU, ROUGE, LLM-as-Judge e RAGAS. Inferência híbrida: Ollama Cloud para geração e juiz, embeddings locais, ChromaDB, traces no LangSmith.

**Resultado:** Melhor RAGAS composto **0.988** com HyDE no Gemma3 27B. Melhor acurácia média de prompting **89.3%** com Qwen3-Coder 480B. Naive RAG continuou competitivo em custo; HyDE colapsou no modelo mais fraco.

**[Repositório](https://github.com/OtnielGomes/LLM-Eval-Suite)**

---

## Stack

**Orquestração e serving**

[![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/langgraph) [![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://www.langchain.com/) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/) [![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

**Recuperação**

[![PostgreSQL](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector) [![ChromaDB](https://img.shields.io/badge/ChromaDB-F97316?style=flat-square)](https://www.trychroma.com/) [![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/)

**Avaliação e observabilidade**

[![RAGAS](https://img.shields.io/badge/RAGAS-6366F1?style=flat-square)](https://docs.ragas.io/) [![LangSmith](https://img.shields.io/badge/LangSmith-FF6B35?style=flat-square)](https://smith.langchain.com/) [![Langfuse](https://img.shields.io/badge/Langfuse-F4B942?style=flat-square)](https://langfuse.com/) [![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)](https://opentelemetry.io/) [![Pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://docs.pytest.org/) [![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=astral&logoColor=white)](https://docs.astral.sh/uv/)

Há um background em modelagem e plataformas de dados (PyTorch, scikit-learn, Spark, Databricks); não é o foco deste perfil.

## Contato

**Otniel Gomes** — AI Engineer · Bauru, SP

- E-mail: [otniel.g.andrade@gmail.com](mailto:otniel.g.andrade@gmail.com)
- LinkedIn: [linkedin.com/in/otnielgomes](https://www.linkedin.com/in/otnielgomes/)
- GitHub: [@OtnielGomes](https://github.com/OtnielGomes)
- Estudos de caso: [Portifolio--AI-Engineering--Data-Science](https://github.com/OtnielGomes/Portifolio--AI-Engineering--Data-Science)
