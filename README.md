<div align="center">

# Santhosh P

**AI / ML Engineer** · Building production-grade AI systems with real architecture decisions

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=15&pause=1200&color=C9184A&center=true&vCenter=true&width=620&lines=Agentic+AI+%7C+LangGraph+%7C+LangChain;FastAPI+%7C+Docker+%7C+Microservices;RAG+Pipelines+%7C+Vector+Search+%7C+MLOps;Next.js+%7C+GitHub+Actions+%7C+CI%2FCD)](https://git.io/typing-svg)

[![GitHub](https://img.shields.io/badge/GitHub-Santhosh--p653-1a0d0f?style=flat-square&logo=github&logoColor=white)](https://github.com/Santhosh-p653)
[![Portfolio](https://img.shields.io/badge/Portfolio-Live-C9184A?style=flat-square&logo=vercel&logoColor=white)](https://santhosh-p653.github.io/doc2site/Santhosh.html)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-santhosh11042007-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/spaces/santhosh11042007/shoppyai)

</div>

---

## What I build

I design and ship AI systems that operate end-to-end — from ingestion and retrieval to agent orchestration and deployment. My projects demonstrate a consistent pattern: structured microservices, production-grade pipelines, and CI/CD from day one.

```python
focus = {
    "core":    ["Agentic AI", "RAG Pipelines", "Computer Vision"],
    "infra":   ["Docker", "GitHub Actions", "FastAPI", "PostgreSQL"],
    "ai":      ["LangGraph", "LangChain", "Qdrant", "ChromaDB"],
    "frontend":["Next.js", "TypeScript", "Gradio"],
    "mantra":  "Make it work. Make it right. Make it fast."
}
```

---

## Skill Map

<table>
<tr>
<td valign="top" width="50%">

**AI / ML**

![LangChain](https://img.shields.io/badge/LangChain-1a0d0f?style=for-the-badge&logo=langchain&logoColor=FF758F)
![LangGraph](https://img.shields.io/badge/LangGraph-1a0d0f?style=for-the-badge&logo=langchain&logoColor=FF758F)
![PyTorch](https://img.shields.io/badge/PyTorch-1a0d0f?style=for-the-badge&logo=pytorch&logoColor=EE4C2C)
![OpenCV](https://img.shields.io/badge/OpenCV-1a0d0f?style=for-the-badge&logo=opencv&logoColor=5C3EE8)
![Transformers](https://img.shields.io/badge/HuggingFace-1a0d0f?style=for-the-badge&logo=huggingface&logoColor=FFD21E)

**Retrieval & Vector DBs**

![Qdrant](https://img.shields.io/badge/Qdrant-1a0d0f?style=for-the-badge&logo=databricks&logoColor=DC244C)
![ChromaDB](https://img.shields.io/badge/ChromaDB-1a0d0f?style=for-the-badge&logo=databricks&logoColor=FF6B35)
![FAISS](https://img.shields.io/badge/FAISS-1a0d0f?style=for-the-badge&logo=meta&logoColor=0467DF)

</td>
<td valign="top" width="50%">

**Backend & APIs**

![FastAPI](https://img.shields.io/badge/FastAPI-1a0d0f?style=for-the-badge&logo=fastapi&logoColor=009688)
![Python](https://img.shields.io/badge/Python-1a0d0f?style=for-the-badge&logo=python&logoColor=FF758F)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a0d0f?style=for-the-badge&logo=postgresql&logoColor=336791)

**Infrastructure & Frontend**

![Docker](https://img.shields.io/badge/Docker-1a0d0f?style=for-the-badge&logo=docker&logoColor=2496ED)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-1a0d0f?style=for-the-badge&logo=githubactions&logoColor=2088FF)
![Next.js](https://img.shields.io/badge/Next.js-1a0d0f?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-1a0d0f?style=for-the-badge&logo=typescript&logoColor=3178C6)
![Linux](https://img.shields.io/badge/Linux-1a0d0f?style=for-the-badge&logo=linux&logoColor=FCC624)

</td>
</tr>
</table>

---

## Projects

### 🕵️ [deepfake-agentic-ai](https://github.com/Santhosh-p653/deepfake-agentic-ai)
**Forensic deepfake detection as a production microservices mesh**

A fully containerized pipeline where each concern — ingestion, ML inference, agent orchestration, and storage — runs in its own Docker service. Uploaded media flows through a `api → agents → ml → agents → api → db` pipeline: FFmpeg and OpenCV handle frame extraction, RetinaFace performs facial localization, Xception extracts forensic texture features, and Transformer models validate temporal coherence across frames. ChromaDB stores facial embeddings for similarity search against known manipulation patterns. MinIO provides object storage with a 30-day auto-expiry lifecycle. FastAPI manages the API layer with structured JSON logging across every module and a Dozzle live log viewer.

```
Stack: Python · FastAPI · LangGraph · Docker Compose · PostgreSQL · ChromaDB · MinIO · RetinaFace · Xception
CI:    GitHub Actions (network audit, logging validation)
```

> **Architecture pattern:** Multi-Dockerfile services (`Dockerfile.api`, `Dockerfile.agents`, `Dockerfile.ml`) with a shared `docker-compose.yml`. Five status stages (`pending → temp_stored → processing → processed → deleted`) tracked in PostgreSQL with full audit trail.

---

### 🧠 [rag-multimodal-assistant](https://github.com/Santhosh-p653/rag-multimodal-assistant)
**Production RAG system with hybrid search, voice, and agentic troubleshooting**

Ingests technical manuals (`PDF`, `DOCX`, `PPTX`, `XLSX`, `TXT`) via Microsoft MarkItDown, chunks them with overlapping context windows, embeds with MiniLM-L6, and stores in Qdrant. Retrieval is a 3-level priority hierarchy — Exact Match → Family Match → Global Match — combining dense and sparse (BM25) candidates through Reciprocal Rank Fusion. The voice layer routes transcription by language: local Whisper for English, Sarvam AI Saaras v3 for Indic languages, and edge-tts for speech synthesis with Microsoft Neural voices. A LangGraph-powered agentic troubleshooting engine guides users through multi-turn diagnostic trees with full session state. Security baked in: `slowapi` rate limiting, MIME-type file guards, regex prompt injection filters, and isolated RAG prompts. Ships with a 24-test suite covering unit, integration, and security checks. Next.js frontend with a dedicated admin upload panel.

```
Stack: Python · FastAPI · LangGraph · Qdrant · BM25 · MiniLM-L6 · Whisper · Sarvam AI · edge-tts
       Next.js · TypeScript · Docker Compose
CI:    GitHub Actions (ruff · black · bandit · detect-secrets)
```

> **Architecture pattern:** Full-stack monorepo (`backend/` + `frontend/`) with Docker Compose. Prompt injection protected at both the regex layer and the LLM system prompt level.

---

### 🛒 [shoppyai](https://github.com/Santhosh-p653/shoppyai) · [Live Demo ↗](https://huggingface.co/spaces/santhosh11042007/shoppyai)
**LLM-powered e-commerce assistant deployed on Hugging Face Spaces**

A natural language product discovery interface built on Gradio with a deliberately extensible backend — designed from day one to evolve from an LLM wrapper into a full RAG retrieval system. The architecture separates the UI layer (`app.py`), inference logic, and a data layer ready for FAISS or ChromaDB integration. Containerized with Docker and deployed publicly on Hugging Face Spaces.

```
Stack: Python · Gradio · Transformers / LLM APIs · Docker · Hugging Face Spaces
CI:    GitHub Actions
```

> **Architecture pattern:** Prompt-orchestration-first design, modular for async inference and vector database integration with zero structural changes.

---

### 📄 [doc2site](https://github.com/Santhosh-p653/doc2site) · [Live ↗](https://santhosh-p653.github.io/doc2site/Santhosh.html)
**Markdown → static site with incremental builds and zero-config GitHub Pages deploy**

A Node.js static site generator that converts Markdown documentation into navigable HTML sites with dark mode toggle, client-side search, and auto-deploy via GitHub Actions on every push. Incremental builds only regenerate changed files. The workflow is a clean example of a CI/CD pipeline with no external services required.

```
Stack: JavaScript · Node.js · GitHub Actions · GitHub Pages
```

> **Architecture pattern:** Source → build → deploy in a single Actions workflow. Demonstrates CI/CD pipeline design for developer tooling.

---

### ⚡ [smart-grid](https://github.com/Santhosh-p653/smart-grid)
**Java-based smart grid energy management system**

An energy infrastructure simulation system modelling smart grid topology and load balancing logic. Demonstrates systems-level thinking in Java, handling grid state transitions and CSS-rendered monitoring views.

```
Stack: Java · CSS
```

---

## GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Santhosh-p653&show_icons=true&theme=tokyonight&hide_border=true&bg_color=130508&title_color=C9184A&icon_color=C9184A&text_color=c9d1d9&rank_icon=github" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Santhosh-p653&layout=compact&theme=tokyonight&hide_border=true&bg_color=130508&title_color=C9184A&text_color=c9d1d9&langs_count=8" />

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com?user=Santhosh-p653&theme=tokyonight&hide_border=true&background=0d1117&ring=C9184A&fire=FF4D6D&currStreakLabel=C9184A" />

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Santhosh-p653&theme=react-dark&hide_border=true&bg_color=130508&color=C9184A&line=00d9ff&point=ffffff)](https://github.com/Santhosh-p653)

</div>

---

## Cross-project patterns

Every project in this portfolio shares a few non-negotiable practices:

- **Containerized from commit one** — Docker and docker-compose across all backend projects
- **CI/CD in every repo** — GitHub Actions for lint, security scan, and deploy
- **Structured logging** — JSON logs to stdout, never print statements
- **Security-first API design** — rate limiting, MIME validation, secret scanning as defaults
- **Separation of concerns** — agents, API, and ML as distinct services, not a monolith

---

<div align="center">

### Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-1a0d0f?style=for-the-badge&logo=linkedin&logoColor=0A66C2)](https://linkedin.com/in/YOUR_LINKEDIN)
[![GitHub](https://img.shields.io/badge/GitHub-1a0d0f?style=for-the-badge&logo=github&logoColor=ffffff)](https://github.com/Santhosh-p653)
[![Portfolio](https://img.shields.io/badge/Portfolio-1a0d0f?style=for-the-badge&logo=vercel&logoColor=FF758F)](https://santhosh-p653.github.io/doc2site/Santhosh.html)

![Profile Views](https://komarev.com/ghpvc/?username=Santhosh-p653&style=for-the-badge&color=C9184A&label=PROFILE+VIEWS)

```
// Open to roles in AI engineering, MLOps, and agentic systems. Let's build.
```

</div>
