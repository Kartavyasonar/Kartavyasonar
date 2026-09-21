<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B22,100:00ADD8&height=220&section=header&text=KARTAVYA%20SONAR&fontSize=48&fontColor=FFFFFF&fontAlignY=38&desc=Backend%20%7C%20Platform%20%7C%20Distributed%20Systems%20%7C%20Applied%20AI&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2800&pause=900&color=00ADD8&center=true&vCenter=true&width=900&lines=Software+Engineer;Python+%7C+Go+%7C+Kubernetes+%7C+Distributed+Systems;Backend+%26+Platform+Engineering;Building+Security+for+AI+Agents;Designing+systems+that+are+observable+and+measurable" alt="Typing animation"/>
</p>

<p align="center">
  <a href="https://github.com/Kartavyasonar"><img src="https://img.shields.io/badge/GitHub-Kartavyasonar-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="https://linkedin.com/in/kartavya-sonar23"><img src="https://img.shields.io/badge/LinkedIn-Kartavya%20Sonar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://kartavyasonar.github.io/"><img src="https://img.shields.io/badge/Portfolio-Website-00ADD8?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
  <a href="mailto:sonarkartavya@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <a href="https://leetcode.com/u/sonarkartavya/"><img src="https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=111111" /></a>
  <a href="https://codeforces.com/profile/Kartavyasonar"><img src="https://img.shields.io/badge/Codeforces-Profile-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" /></a>
  <a href="https://drive.google.com/file/d/1-AGCOuY3D7ZFyIm9LYpPwO-6G8LcLSHN/view?usp=sharing"><img src="https://img.shields.io/badge/CV-View-8B949E?style=for-the-badge&logo=googledrive&logoColor=white" /></a>
</p>

---

# 👨‍💻 About Me

I am a software engineer focused on **backend systems, distributed infrastructure, developer tooling, and applied AI**.

I enjoy working where software meets systems engineering: designing APIs, asynchronous services, retrieval pipelines, agent architectures, security boundaries, observability, and cloud-native infrastructure.

My engineering interests include:

- Backend and API infrastructure
- Distributed systems and asynchronous processing
- Kubernetes and cloud-native systems
- AI agents, RAG, retrieval and memory
- AI-agent and MCP security
- Databases, caching and messaging
- Observability, benchmarking and reliability
- Open-source engineering

I care about **clear system boundaries, correctness, measurable behaviour, maintainability, and understanding how software behaves under real constraints.**

### 🎓 Education

**MSc Advanced Computer Science — University of Leeds**  
2024–2025 · Merit

Relevant areas included algorithms, data science, machine learning, deep learning, data mining and text analysis, cloud computing systems and blockchain technologies.

**B.Tech Computer Science — GGSIPU / Delhi Technical Campus**  
2021–2024 · CGPA 8.24

**Diploma in Computer Technology — MSBTE**  
2018–2021 · 87.09%

---

# 🔭 Currently Building

## 🛡️ InvokeCordon

An open-source **MCP security scanner and runtime JSON-RPC gateway**.

The project is focused on placing a security boundary between an AI client and MCP servers so that tool descriptions and tool invocations can be inspected before they reach downstream systems.

The design explores:

- Tool poisoning detection
- Prompt-injection-oriented checks
- Runtime policy enforcement
- Secret redaction
- Audit logging
- JSON-RPC interception
- Prometheus metrics
- Security-oriented tool validation

> AI Client → Security Gateway → MCP Server

Repository:  
**https://github.com/Kartavyasonar/toolgate**

---

# 🛡️ InvokeCordon — Architecture

```text
                         AI CLIENT
                            │
                            │ MCP / JSON-RPC
                            ▼
                ┌─────────────────────────┐
                │       INVOKECORDON      │
                │                         │
                │   Security Gateway      │
                └────────────┬────────────┘
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
          ▼                  ▼                  ▼
    ┌───────────┐      ┌────────────┐    ┌─────────────┐
    │   Tool    │      │   Policy   │    │   Secret    │
    │  Scanner  │      │   Engine   │    │  Redaction  │
    └───────────┘      └────────────┘    └─────────────┘
          │                  │                  │
          └──────────────────┼──────────────────┘
                             ▼
                    ┌────────────────┐
                    │  Audit / Hash  │
                    │  Observability │
                    └───────┬────────┘
                            │
                            ▼
                       MCP SERVER
```

### Core Security Model

| Layer | Responsibility |
|---|---|
| Tool Scanner | Inspect MCP tool definitions and identify suspicious characteristics |
| Policy Engine | Decide whether a tool call should be allowed, denied or observed |
| Request Validation | Inspect JSON-RPC/tool-call structure before forwarding |
| Secret Redaction | Remove sensitive values from logged or exposed payloads |
| Audit Logging | Preserve security-relevant execution history |
| Metrics | Expose runtime behaviour for Prometheus |
| Gateway | Keep the AI client isolated from direct MCP-server access |

---

# ☸️ Kubernetes & Open Source

I have contributed to Kubernetes-related infrastructure and testing work.

### 🔹 PR #138993 — Rootless Namespace Testing

Added `RunInUserNS()` support for re-executing test binaries inside unprivileged Linux user and network namespaces, enabling rootless kube-proxy nftables testing.

**Focus:** Linux namespaces · rootless testing · kube-proxy · networking

[View PR →](https://github.com/kubernetes/kubernetes/pull/138993)

### 🔹 PR #37058 — Prow Presubmit CI

Added Prow presubmit CI jobs gated by custom build tags for namespace-isolation testing.

**Focus:** CI/CD · Prow · Kubernetes test infrastructure

[View PR →](https://github.com/kubernetes/test-infra/pull/37058)

### 🔹 Issue #139170 — ConfigMap BinaryData

Worked on documenting and validating Kubernetes API behaviour around `ConfigMap.BinaryData`.

**Focus:** Kubernetes API · ConfigMap · API behaviour/documentation

[View Issue →](https://github.com/kubernetes/kubernetes/issues/139170)

---

# 🚀 Engineering Work

<details>
<summary><b>⚡ PulseAPI — Distributed API Gateway</b></summary>

### Stack

`Node.js` `Redis` `Kafka` `PostgreSQL` `Prometheus` `Grafana` `k6`

A distributed API gateway designed around rate limiting, asynchronous processing, persistence and observability.

### Engineering Areas

- Redis-backed rate limiting
- Atomic operations using Redis Lua
- Sliding-window request control
- Distributed circuit-breaker state
- Kafka-based asynchronous event/log processing
- PostgreSQL persistence
- Prometheus metrics
- Grafana dashboards
- k6 load testing

### Recorded Benchmark

```text
Throughput       : 207 req/s
p99 latency      : 881 ms
Error rate       : 0.0%
```

</details>

---

<details>
<summary><b>🧠 GhostMind — Self-Evolving Research Agent</b></summary>

### Stack

`Python` `FastAPI` `FAISS` `NetworkX` `React` `Vite` `SQLite`

A research-oriented agent combining retrieval, graph structure and episodic memory.

### Retrieval Strategies

```text
                    USER QUERY
                         │
                         ▼
                ┌────────────────┐
                │ Strategy Layer │
                └───────┬────────┘
                        │
          ┌─────────────┼─────────────┐
          ▼             ▼             ▼
      Semantic        Hybrid        Graph
          │             │             │
          └─────────────┼─────────────┘
                        ▼
                 Query Rewrite
                        │
                        ▼
                    Retrieval
                        │
                        ▼
                     LLM
                        │
                        ▼
                    Outcome
                        │
                        ▼
               Episodic Memory
```

The system stores the relationship between **intent, selected strategy and observed outcome**, allowing later queries to use previous retrieval experience.

</details>

---

<details>
<summary><b>🤖 Multi-Agent AI Code Review Platform</b></summary>

### Stack

`Python` `LangGraph` `ChromaDB` `Groq LLaMA` `FastAPI` `React` `Vite` `Docker`

A multi-agent code-review system that combines static analysis, retrieval and specialist agents.

### Review Pipeline

```text
Repository
    │
    ▼
Clone / Inspect
    │
    ├──────────────► Python AST
    │
    ├──────────────► Radon / Complexity
    │
    ▼
Function-level chunks
    │
    ▼
Embeddings / ChromaDB
    │
    ▼
┌──────────────────────────────────┐
│          SPECIALIST AGENTS       │
│                                  │
│  Bug │ Security │ Performance    │
│            │ Quality             │
└─────────────────┬────────────────┘
                  ▼
             Synthesizer
                  │
                  ▼
          Structured Report
```

The project also streams review progress to the frontend using SSE.

Repository:  
**https://github.com/Kartavyasonar/AI-CODE-REVIEW**

Live frontend:  
**https://ai-code-review-xi-one.vercel.app/**

</details>

---

<details>
<summary><b>🌐 NetPulse — Distributed Network Monitoring</b></summary>

### Stack

`FastAPI` `PostgreSQL` `NetworkX` `Scapy` `Nmap` `React` `Recharts` `Docker`

A network operations platform that monitors topology and network health from multiple geographic or logical vantage points.

### Backend

- FastAPI / Uvicorn
- SQLAlchemy async
- asyncpg
- Alembic
- Pydantic v2
- APScheduler
- NetworkX
- Scapy
- python-nmap
- httpx
- NumPy / Pandas

### Frontend

- React 18
- React Router
- Recharts
- react-force-graph-2d
- Axios
- Tailwind
- Vite

### Infrastructure

`PostgreSQL 16` · `Docker Compose` · `Nginx` · `Let's Encrypt` · `Oracle Cloud` · `Vercel`

Repository:  
**https://github.com/Kartavyasonar/NetPulse**

</details>

---

<details>
<summary><b>⚖️ NYAYA AI — Multilingual Legal RAG</b></summary>

### Stack

`FastAPI` `FAISS` `BM25` `Reranking` `Groq LLaMA` `MongoDB Atlas` `Twilio`

An AI legal-information assistant designed around multilingual access to Indian legal and government information.

### Retrieval Pipeline

```text
User Query
    │
    ▼
Language / Query Processing
    │
    ├──────────────┐
    ▼              ▼
 Dense Search   Sparse Search
  (FAISS)         (BM25)
    │              │
    └──────┬───────┘
           ▼
       Reranking
           │
           ▼
      LLM Response
```

Knowledge sources include Indian constitutional/legal material, legislation, government schemes and selected judgments.

</details>

---

<details>
<summary><b>✈️ WanderPlan — AI Travel Planner</b></summary>

### Stack

`React` `Vite` `Node.js` `Express` `PostgreSQL` `Leaflet` `OpenStreetMap`

AI-assisted travel planning with maps, weather, cost estimates, packing lists, voice narration, calendar export, trip history and PWA support.

Live:  
**https://wander-plan-orcin.vercel.app/**

Repository:  
**https://github.com/Kartavyasonar/WanderPlan**

</details>

---

<details>
<summary><b>☁️ Serverless / FaaS Performance Benchmark</b></summary>

### Stack

`Azure Functions` `OpenFaaS` `K3s` `Kubernetes` `Docker` `Helm` `Apache JMeter`

Compared equivalent Python inference endpoints across managed Azure Functions and self-hosted OpenFaaS/K3s.

### Measured Areas

- Latency
- Throughput
- Cold starts
- Concurrency
- Scalability
- Error rate

The study focused on the engineering trade-off between managed serverless simplicity and the control/predictability available from self-hosted infrastructure.

</details>

---

# 🔬 Research

## Mapping Public Emotion in Digital Governance

**MSc research project — UK immigration discourse on Reddit**

Dataset:

```text
1,098 Reddit posts
```

Methods included:

- BERTopic
- Transformer-based emotion analysis
- Topic/discourse analysis
- Semantic matching
- UK legislation mapping
- Streamlit-based analysis dashboard

The work examined how public emotion and discourse themes appear in online discussions surrounding UK immigration and digital governance.

Publication:

**“Mapping Public Emotion in Digital Governance: A Comparative NLP Analysis of UK Immigration Discourse on Reddit”**

---

# 🧰 Tech Stack

### Languages

<p>
<img src="https://skillicons.dev/icons?i=python,go,java,cpp,js,ts,bash&perline=8" />
</p>

`Python` · `Go` · `Java` · `C++` · `JavaScript` · `TypeScript` · `SQL` · `Bash`

### Backend

`FastAPI` · `Node.js` · `REST APIs` · `Async Python` · `Microservices` · `JSON-RPC`

### Distributed Systems

`Kafka` · `Redis` · `PostgreSQL` · `Kubernetes` · `Docker`

### AI / Retrieval

`LLMs` · `RAG` · `FAISS` · `ChromaDB` · `Embeddings` · `LangGraph` · `NetworkX` · `Hugging Face`

### Cloud / Infrastructure

<p>
<img src="https://skillicons.dev/icons?i=aws,gcp,kubernetes,docker,linux,nginx,githubactions&perline=8" />
</p>

`AWS` · `GCP` · `Kubernetes` · `Docker` · `Linux` · `Nginx` · `GitHub Actions`

### Observability

`Prometheus` · `Grafana` · `k6`

### Databases

`PostgreSQL` · `MongoDB` · `Redis` · `SQLite` · `MySQL`

---

# 📊 GitHub Snapshot

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Kartavyasonar&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github" height="175"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kartavyasonar&layout=compact&theme=github_dark&hide_border=true" height="175"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Kartavyasonar&theme=dark&hide_border=true&background=00000000&ring=00ADD8&fire=FF6B35&currStreakNum=FFFFFF&sideNums=FFFFFF&currStreakLabel=FFFFFF&sideLabels=FFFFFF&dates=FFFFFF" width="75%"/>
</p>

---

# 📈 Contribution Activity

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Kartavyasonar&bg_color=0D1117&color=C9D1D9&line=00ADD8&point=FFFFFF&area=true&hide_border=true&custom_title=GitHub%20Contribution%20Activity" width="96%"/>
</p>

---

# 🧩 Featured Projects

<table>
<tr>
<td width="50%">

### 🛡️ InvokeCordon

**MCP Security Gateway**

`Go` · `MCP` · `JSON-RPC` · `Prometheus`

Security boundary for AI-agent tool execution.

**[Repository →](https://github.com/Kartavyasonar/toolgate)**

</td>

<td width="50%">

### ⚡ PulseAPI

**Distributed API Gateway**

`Node.js` · `Redis` · `Kafka` · `PostgreSQL`

Caching, rate limiting, circuit breaking and observability.

</td>
</tr>

<tr>
<td width="50%">

### 🧠 GhostMind

**Self-Evolving Research Agent**

`Python` · `FAISS` · `NetworkX` · `FastAPI`

Retrieval strategy selection with episodic memory.

</td>

<td width="50%">

### 🤖 AI Code Review

**Multi-Agent Code Analysis**

`LangGraph` · `ChromaDB` · `AST` · `Radon`

Specialist agents for bugs, security, quality and performance.

**[Repository →](https://github.com/Kartavyasonar/AI-CODE-REVIEW)**

</td>
</tr>

<tr>
<td width="50%">

### 🌐 NetPulse

**Network Operations Platform**

`FastAPI` · `NetworkX` · `PostgreSQL` · `React`

Topology monitoring and anomaly detection.

**[Repository →](https://github.com/Kartavyasonar/NetPulse)**

</td>

<td width="50%">

### ✈️ WanderPlan

**AI Travel Planner**

`React` · `Node.js` · `PostgreSQL` · `Leaflet`

AI planning, maps, weather and trip management.

**[Live →](https://wander-plan-orcin.vercel.app/)**

</td>
</tr>
</table>

---

# 🧠 Engineering Principles

```text
01  Measure before optimizing
02  Keep system boundaries explicit
03  Prefer simple primitives when they are enough
04  Make failure observable
05  Treat security as part of architecture
06  Benchmark the behaviour you claim
07  Automate repetitive operational work
08  Design for debugging, not only the happy path
```

---

# 🎯 Current Focus

```text
┌─────────────────────────────────────────────────────┐
│                                                     │
│  BACKEND SYSTEMS                                    │
│       │                                             │
│       ├──► Distributed APIs                         │
│       ├──► Async processing                         │
│       ├──► Databases / caching                      │
│       │                                             │
│       ▼                                             │
│  CLOUD-NATIVE INFRASTRUCTURE                        │
│       │                                             │
│       ├──► Kubernetes                               │
│       ├──► Containers                               │
│       ├──► Observability                            │
│       │                                             │
│       ▼                                             │
│  APPLIED AI                                         │
│       │                                             │
│       ├──► Agents                                   │
│       ├──► Retrieval / RAG                          │
│       ├──► Memory                                   │
│       │                                             │
│       ▼                                             │
│  AI SECURITY                                        │
│       │                                             │
│       ├──► MCP                                      │
│       ├──► Tool security                            │
│       ├──► Policy enforcement                       │
│       └──► Auditing                                 │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

# 📫 Connect

<p align="center">
  <a href="https://github.com/Kartavyasonar"><img src="https://img.shields.io/badge/GitHub-Kartavyasonar-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="https://linkedin.com/in/kartavya-sonar23"><img src="https://img.shields.io/badge/LinkedIn-Kartavya%20Sonar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:sonarkartavya@gmail.com"><img src="https://img.shields.io/badge/Email-sonarkartavya%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <sub>Built around systems, measured by behaviour, improved through iteration.</sub>
</p>
