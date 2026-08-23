<div align="center">

<img src="https://api.dicebear.com/7.x/bottts/svg?seed=Scout&backgroundColor=0d1b3e&primaryColorLevel=600&baseColor=1e40af,3b82f6&eyes=bulging&mouth=grill02" width="1" height="1" alt="" />

<!-- ══════════════ COLD OPEN ══════════════ -->

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=15&duration=2500&pause=800&color=6EA8FE&center=true&vCenter=true&width=700&lines=connection+established...;two+agents+detected+on+this+channel;SCOUT-7+%E2%86%94+SANTHOSH.exe)](https://git.io/typing-svg)

<br>

<table>
<tr>
<td align="center" width="140">
<img src="https://api.dicebear.com/7.x/bottts/svg?seed=ScoutAgent&backgroundColor=0d1b3e&baseColor=1e40af,3b82f6&eyes=bulging" width="90" height="90" style="border-radius:50%;border:2px solid #3b82f6" />
<br><b><sub>SCOUT-7</sub></b>
<br><sub><i>talent-recon unit</i></sub>
</td>
<td align="center" width="60"><h2>⇄</h2></td>
<td align="center" width="140">
<img src="https://api.dicebear.com/7.x/bottts/svg?seed=SanthoshAgent&backgroundColor=0d1b3e&baseColor=2563eb,60a5fa&eyes=roundOff" width="90" height="90" style="border-radius:50%;border:2px solid #60a5fa" />
<br><b><sub>SANTHOSH.exe</sub></b>
<br><sub><i>engineer runtime</i></sub>
</td>
</tr>
</table>

</div>

<br>

<div align="center">

```
◈ TRANSCRIPT LOG — CHANNEL #build-verify — SESSION OPEN ◈
```

</div>

<br>

> 🔵 **SCOUT-7:** New signal on the network. Runtime, identify yourself.

> 🔷 **SANTHOSH.exe:** Santhosh — 3rd year CSE, Karpagam Institute of Technology. I don't build demos, I build things that stay up after the deploy.

---

<br>

### `Q01` — *"What's your actual operating principle?"*

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=14&duration=2200&pause=900&color=5B8DEF&center=true&vCenter=true&width=620&lines=Make+it+work.;Make+it+right.;Make+it+fast.;Then+containerize+it+and+walk+away.)](https://git.io/typing-svg)

</div>

<details open>
<summary><b>🔷 SANTHOSH.exe — expand full answer</b></summary>
<br>

Every system I ship follows the same invariants, no exceptions:

| Invariant | Enforced by |
|---|---|
| Containerized from commit one | Docker / Docker Compose |
| CI/CD in every repo | GitHub Actions — lint · security scan · deploy |
| JSON structured logging | stdout, never `print()` |
| Security-first APIs | rate limiting · MIME guards · Bandit · detect-secrets |
| Separation of concerns | agents ≠ API ≠ ML, always separate services |

</details>

<br>

> 🔵 **SCOUT-7:** Noted. Running a scan on your module registry now.

---

<br>

### `Q02` — *"What's actually in your stack?"*

<details>
<summary><b>🔷 SANTHOSH.exe — tap to expand the module registry</b></summary>
<br>

**`MODULE 01` — AI Core**

<img src="https://skillicons.dev/icons?i=pytorch,opencv,py&theme=dark" />

`LangGraph` · `LangChain` · `PyTorch` · `OpenCV` · `Transformers` · `Whisper` · `Sarvam AI Saaras v3` · `edge-tts`

**`MODULE 02` — Retrieval Layer**

<img src="https://skillicons.dev/icons?i=py&theme=dark" />

`Qdrant` · `ChromaDB` · `FAISS` · `BM25 + RRF fusion` · `MarkItDown` · `MiniLM-L6`

**`MODULE 03` — Backend**

<img src="https://skillicons.dev/icons?i=fastapi,python,postgres&theme=dark" />

`FastAPI` · `Python` · `PostgreSQL` · `MinIO`

**`MODULE 04` — Infra / DevOps**

<img src="https://skillicons.dev/icons?i=docker,githubactions,linux&theme=dark" />

`Docker Compose` · `GitHub Actions` · `Bandit` · `ruff` · `Dozzle`

**`MODULE 05` — Frontend**

<img src="https://skillicons.dev/icons?i=nextjs,typescript,nodejs&theme=dark" />

`Next.js` · `TypeScript` · `Gradio` · `GitHub Pages`

</details>

<br>

> 🔵 **SCOUT-7:** Four production repos flagged. Walk me through them — one at a time. Start with the one that scares you most.

---

<br>

## `THREAD 01` — deepfake-agentic-ai 🕵️

![status](https://img.shields.io/badge/STATUS-DEPLOYED-1e3a8a?style=flat-square&labelColor=0d1b3e) [![repo](https://img.shields.io/badge/REPO-source-3b82f6?style=flat-square&logo=github&logoColor=white)](https://github.com/Santhosh-p653/deepfake-agentic-ai)

> 🔵 **SCOUT-7:** Problem statement?

> 🔷 **SANTHOSH.exe:** Deepfakes are spreading faster than single-model detectors can keep up. One model, one point of failure, zero auditability. So I didn't build a model — I built a forensic mesh.

<details>
<summary>🔷 <b>show me the mesh</b></summary>

```mermaid
flowchart LR
    U[Upload] --> API[API Gateway]
    API --> AG[Agent Orchestrator]
    AG --> ML[ML Service]
    ML --> RF[RetinaFace]
    ML --> XC[Xception CNN]
    ML --> TR[Transformers]
    AG --> CH[(ChromaDB)]
    AG --> PG[(PostgreSQL)]
    PG --> MI[(MinIO)]
    MI --> EX[Auto-Expiry 30d]

    style U fill:#3b82f6,stroke:#0d1b3e,color:#fff
    style API fill:#0d1b3e,stroke:#3b82f6,color:#fff
    style AG fill:#0d1b3e,stroke:#3b82f6,color:#fff
    style ML fill:#0d1b3e,stroke:#3b82f6,color:#fff
```

</details>

> 🔵 **SCOUT-7:** What happens when the signals disagree with each other?

> 🔷 **SANTHOSH.exe:** `FLAG_FOR_REVIEW` isn't a failure state — it's the honest one. Multi-signal weighted aggregation surfaces uncertainty instead of forcing a binary call it can't defend.

`Python` · `FastAPI` · `LangGraph` · `PostgreSQL` · `ChromaDB` · `MinIO` · `RetinaFace` · `Xception` — three isolated Dockerfiles (`api` / `agents` / `ml`), one compose mesh, JSON logs streamed live to Dozzle.

---

<br>

## `THREAD 02` — rag-multimodal-assistant 🧠

![status](https://img.shields.io/badge/STATUS-DEPLOYED-1e3a8a?style=flat-square&labelColor=0d1b3e) [![repo](https://img.shields.io/badge/REPO-source-3b82f6?style=flat-square&logo=github&logoColor=white)](https://github.com/Santhosh-p653/rag-multimodal-assistant)

> 🔵 **SCOUT-7:** Next thread.

> 🔷 **SANTHOSH.exe:** Enterprise manuals live in a graveyard of PDFs and PPTX files. Users either dig by hand or get generic LLM hallucinations — and none of it speaks Tamil or Hindi. So I built retrieval, voice, and diagnosis as one agentic system.

<details>
<summary>🔷 <b>show me the retrieval fusion</b></summary>

```mermaid
flowchart LR
    Q[Query] --> M1[Exact Match]
    M1 --> M2[Family Match]
    M2 --> M3[Global Match]
    M1 --> DV[Dense Vector]
    M2 --> BM[BM25 Sparse]
    M3 --> RRF[RRF Fusion]
    DV --> RRF
    BM --> RRF
    RRF --> LLM[LLM]

    style Q fill:#3b82f6,stroke:#0d1b3e,color:#fff
    style RRF fill:#0d1b3e,stroke:#3b82f6,color:#fff
    style LLM fill:#0d1b3e,stroke:#3b82f6,color:#fff
```

</details>

<details>
<summary>🔷 <b>show me the voice layer</b></summary>

```mermaid
flowchart LR
    subgraph eng["English Path"]
        EA[English Audio] --> W[Whisper STT] --> R1[Response] --> T1[edge-tts]
    end
    subgraph indic["Indic Path"]
        IA[Indic Audio] --> S[Sarvam Saaras v3] --> R2[Response] --> T2[edge-tts]
    end
```

</details>

> 🔵 **SCOUT-7:** Anyone can bolt on a chatbot. What stops someone from prompt-injecting your knowledge base?

> 🔷 **SANTHOSH.exe:** Two layers — regex filtering, then isolated RAG prompts at the LLM system-prompt level. Backed by a 24-test suite covering unit, integration, and security cases.

`Python` · `FastAPI` · `LangGraph` · `Qdrant` · `BM25` · `Whisper` · `Sarvam AI` · `Next.js` · `TypeScript` — full-stack monorepo, `ruff` + `black` + `bandit` + `detect-secrets` on every push.

<sub>🔷 *Phase 3 in flight: multi-provider LLM key rotation (Gemini → Groq → SambaNova → HF → OpenAI), VLM image captioning, parent-child chunking, BGE reranker.*</sub>

---

<br>

## `THREAD 03` — shoppyai 🛒

![status](https://img.shields.io/badge/STATUS-LIVE-1e3a8a?style=flat-square&labelColor=0d1b3e) [![repo](https://img.shields.io/badge/REPO-source-3b82f6?style=flat-square&logo=github&logoColor=white)](https://github.com/Santhosh-p653/shoppyai) [![demo](https://img.shields.io/badge/DEMO-live-60a5fa?style=flat-square&logo=huggingface&logoColor=white)](https://huggingface.co/spaces/santhosh11042007/shoppyai)

> 🔵 **SCOUT-7:** This one's public. Why?

> 🔷 **SANTHOSH.exe:** E-commerce search is still keyword matching in 2026. People describe what they want in plain language — the catalog just doesn't listen. So I made it listen, and put it where anyone can poke at it.

```mermaid
flowchart TD
    U[Natural Language Query] --> G[Gradio UI]
    G --> IL[Inference Logic]
    IL --> API[LLM API]
    IL --> DL[Data Layer]
    DL --> VDB[FAISS / ChromaDB ready]
    G --> DK[Docker Container]
    DK --> HF[HuggingFace Spaces]

    style U fill:#3b82f6,stroke:#0d1b3e,color:#fff
    style HF fill:#0d1b3e,stroke:#60a5fa,color:#fff
```

`Python` · `Gradio` · `Transformers / LLM APIs` · `Docker` · `HF Spaces` — prompt-orchestration-first, ready for async inference and a vector DB swap with zero structural rewrite.

---

<br>

## `THREAD 04` — doc2site 📄

![status](https://img.shields.io/badge/STATUS-DEPLOYED-1e3a8a?style=flat-square&labelColor=0d1b3e) [![repo](https://img.shields.io/badge/REPO-source-3b82f6?style=flat-square&logo=github&logoColor=white)](https://github.com/Santhosh-p653/doc2site) [![live](https://img.shields.io/badge/LIVE-portfolio-60a5fa?style=flat-square&logo=vercel&logoColor=white)](https://santhosh-p653.github.io/doc2site/Santhosh.html)

> 🔵 **SCOUT-7:** Last one. Smallest scope?

> 🔷 **SANTHOSH.exe:** Markdown docs shouldn't need a CMS to be readable on the web. Push a `.md`, get a themed, searchable static site — nothing more.

```mermaid
flowchart LR
    A[Markdown Source] --> B[Node.js Build]
    B --> C[HTML + Dark Mode + Search]
    C --> D[GitHub Actions]
    D --> E[GitHub Pages]
    B --> F[Incremental — only changed files rebuilt]

    style A fill:#3b82f6,stroke:#0d1b3e,color:#fff
    style E fill:#0d1b3e,stroke:#60a5fa,color:#fff
```

`JavaScript` · `Node.js` · `GitHub Actions` · `GitHub Pages` — incremental builds via MD5 hashing.

---

<br>

### `Q_FINAL` — *"Prove it. Show me the telemetry."*

> 🔵 **SCOUT-7:** Talk is cheap. Pull your live numbers.

> 🔷 **SANTHOSH.exe:** Don't take my word for it — this queries GitHub directly, every time this page loads.

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Santhosh-p653&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1b3e&title_color=6EA8FE&icon_color=6EA8FE&text_color=c9d9f5&rank_icon=github" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Santhosh-p653&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1b3e&title_color=6EA8FE&text_color=c9d9f5&langs_count=8" />

<br>

<img src="https://github-readme-streak-stats.herokuapp.com?user=Santhosh-p653&theme=tokyonight&hide_border=true&background=0d1b3e&ring=3b82f6&fire=6EA8FE&currStreakLabel=6EA8FE" />

<br>

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Santhosh-p653&theme=react-dark&hide_border=true&bg_color=0d1b3e&color=3b82f6&line=6EA8FE&point=ffffff)](https://github.com/Santhosh-p653)

</div>

<div align="center">

| Metric | Value |
|---|---|
| Deployed production repos | 4 |
| Independent microservices shipped | 8+ (API · Agents · ML across 2 systems) |
| CI/CD coverage | 100% of repos |
| Containerized services | 100% |
| Voice/ASR languages | English · Tamil · Hindi |

</div>

---

<br>

> 🔵 **SCOUT-7:** Verified. Logging you as a match. Where do I route the offer?

> 🔷 **SANTHOSH.exe:** Anywhere below. Open to AI engineering, MLOps, and agentic-systems roles — I build production systems, not demos.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![GitHub](https://img.shields.io/badge/GitHub-0d1b3e?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Santhosh-p653)
[![Portfolio](https://img.shields.io/badge/Portfolio-3b82f6?style=for-the-badge&logo=vercel&logoColor=white)](https://Santhosh-p653.github.io/portfolio/)

<br>

![Profile Views](https://komarev.com/ghpvc/?username=Santhosh-p653&style=for-the-badge&color=3b82f6&label=PROFILE+VIEWS)

<br>

```
◈ CHANNEL #build-verify — SESSION CLOSED — both agents nominal ◈
```

</div>
