<h1 align="center">Hi, I'm Sanjay 👋</h1>
<h3 align="center">AI Engineer — Agentic Systems & RAG</h3>

<p align="center">
  Fresher AI Engineer based in India, building agentic AI systems with FastAPI and LLMs.
  Not academic/research-focused — I learn by shipping working systems.
</p>

<p align="center">
  📫 kcsanjayj@gmail.com &nbsp;|&nbsp;
  <a href="https://linkedin.com/in/kcsanjayj">LinkedIn</a> &nbsp;|&nbsp;
  🇮🇳 India (open to remote/hybrid)
</p>

---

### About

I build agentic AI systems — planner/executor/critic architectures, RAG pipelines with
self-evaluation, and multi-LLM orchestration. My background is a hands-on ML internship
plus two solo projects where I designed the full system myself: planning, execution,
failure handling, and evaluation loops, not just a single prompt wrapped in an API.

I'm upfront about scope: these are engineering demonstrations, not production platforms.
Both project READMEs list what's missing (tests, sandboxing, CI/CD) because I'd rather be
accurate than impressive.

---

### 🔧 What I actually work with

**Languages**
<p><img src="https://skillicons.dev/icons?i=python,mysql,js" /></p>

**AI / Agentic**
<p><img src="https://skillicons.dev/icons?i=langchain,pytorch" />
&nbsp;<img src="https://img.shields.io/badge/RAG-black?style=for-the-badge&logo=databricks&logoColor=white" height="48"/>
&nbsp;<img src="https://img.shields.io/badge/Multi--Agent-black?style=for-the-badge&logo=semanticweb&logoColor=white" height="48"/></p>

**Backend**
<p><img src="https://skillicons.dev/icons?i=fastapi,python" />
&nbsp;<img src="https://img.shields.io/badge/REST_API-black?style=for-the-badge&logo=fastapi&logoColor=white" height="48"/></p>

**Data**
<p><img src="https://skillicons.dev/icons?i=mysql,chromadb" /></p>

**Infra**
<p><img src="https://skillicons.dev/icons?i=docker,git,aws" /></p>

---

### 🚀 Featured Projects

#### [Dragonite](https://github.com/kcsanjayj/Dragonite) — Graph-based multi-agent orchestrator
Converts a user request into a dependency-aware task DAG, then runs it through
Planner → Executor → Critic → Replanner → Synthesizer.

- Independent tasks execute in parallel; dependent tasks wait on prerequisites
- Configurable retry with backoff on task failure
- Critic stage can reject weak output and trigger a repair/replan cycle instead of
  returning it
- Shared LLM client across planner/executor/synthesizer to avoid duplicated config
- Built on Google ADK

**Stack:** Python 3.11, Google ADK, FastAPI, Pydantic, ThreadPoolExecutor, OpenTelemetry

---

#### [Aetherion](https://github.com/kcsanjayj/Aetherion) — Self-correcting RAG system
A RAG pipeline where every answer is scored by a critic agent before it reaches the
user, with a bounded retry loop for low-quality responses.

- Generate → Evaluate → Refine → Finalize pipeline (not a single retrieval+generate call)
- Critic agent scores responses and gives specific feedback for retry ("missing
  citations", "too shallow") rather than a blind regenerate
- Multi-LLM fallback across 7+ providers (OpenAI, Anthropic, Groq, HuggingFace, etc.)
  for timeout/failure recovery
- Retries are bounded — explicitly avoids infinite refinement loops
- Async FastAPI backend, ChromaDB for retrieval

**Live demo:** https://agentic-rag-gamma.vercel.app

**Stack:** FastAPI, ChromaDB, OpenAI/Anthropic/Groq, sentence-transformers, Docker, Railway

---

### 💼 Experience

**Machine Learning Intern — Tringapps Research Labs**
Built LangChain automation workflows, FastAPI microservices for AI integrations, and
optimized LLM prompt pipelines. Took what I learned there directly into Aetherion and
Dragonite as personal projects.

---

### 🎯 Looking for

AI/ML or backend roles where the work is real LLM systems — agentic pipelines, RAG,
AI infrastructure — not tutorial-tier chatbot integrations.

---

<p align="center"><i>Learning by building — production-inspired, not production-claimed.</i></p>
