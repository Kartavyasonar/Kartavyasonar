<!-- =========================
     ANIMATED HEADER
========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B22,100:00ADD8&height=220&section=header&text=KARTAVYA%20SONAR&fontSize=48&fontColor=FFFFFF&fontAlignY=38&desc=Backend%20%7C%20Platform%20%7C%20Cloud-Native%20%7C%20AI%20Security&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>
</p>

<!-- =========================
     TYPING ANIMATION
========================= -->

<p align="center">
  <a href="https://github.com/Kartavyasonar">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2800&pause=900&color=00ADD8&center=true&vCenter=true&width=850&lines=Backend+%26+Platform+Engineer;Go+%7C+Python+%7C+Kubernetes+%7C+Distributed+Systems;Kubernetes+Open+Source+Contributor;Building+ToolGate+%E2%80%94+Security+for+AI+Agents;Designing+systems+that+scale%2C+fail+gracefully%2C+and+stay+observable" alt="Typing animation"/>
  </a>
</p>

<!-- =========================
     SOCIAL / PROFILE BADGES
========================= -->

<p align="center">

<a href="https://github.com/Kartavyasonar">
<img src="https://img.shields.io/badge/GitHub-Kartavyasonar-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="https://linkedin.com/in/kartavya-sonar23">
<img src="https://img.shields.io/badge/LinkedIn-Kartavya%20Sonar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>

<a href="https://kartavyasonar.github.io/">
<img src="https://img.shields.io/badge/Portfolio-Website-00ADD8?style=for-the-badge&logo=googlechrome&logoColor=white" />
</a>

<a href="mailto:sonarkartavya@gmail.com">
<img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

</p>

<p align="center">

<img src="https://komarev.com/ghpvc/?username=Kartavyasonar&style=for-the-badge&color=00ADD8&label=PROFILE+VIEWS" />

<a href="https://github.com/Kartavyasonar?tab=followers">
<img src="https://img.shields.io/github/followers/Kartavyasonar?style=for-the-badge&logo=github&label=FOLLOWERS" />
</a>

<a href="https://github.com/Kartavyasonar?tab=repositories">
<img src="https://img.shields.io/github/stars/Kartavyasonar?style=for-the-badge&logo=github&label=STARS" />
</a>

</p>

---

# 👨‍💻 About Me

I build infrastructure that scales, fails gracefully, and can be observed.

My engineering focus is on:

- High-throughput backend systems
- Concurrent Go services
- Distributed systems
- Kubernetes and cloud-native infrastructure
- API infrastructure
- AI agent security
- Observability and reliability engineering

I care about **correctness, clean system boundaries, measurable performance, and systems that survive real load.**

### 🔭 Currently Building

**[ToolGate](https://github.com/Kartavyasonar/toolgate)**

An open-source security gateway for MCP servers, written in Go.

It scans MCP tools for security risks and acts as a runtime JSON-RPC policy gateway between AI agents and MCP servers.

### 🌱 Open Source

Active contributor to:

**[Kubernetes](https://github.com/kubernetes/kubernetes)**

with work around rootless namespace testing, kube-proxy testing, Prow CI, and Kubernetes API behavior.

### ⚡ Engineering Focus

```text
Distributed Systems
        │
        ├── Go
        ├── Python
        ├── Kubernetes
        ├── PostgreSQL
        ├── Redis
        ├── Kafka
        ├── Prometheus
        └── OpenTelemetry
```

---

# 🛡️ ToolGate

<p align="center">

<a href="https://github.com/Kartavyasonar/toolgate">
<img src="https://img.shields.io/badge/ToolGate-MCP%20Security%20Gateway-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
</a>

<img src="https://img.shields.io/badge/Language-Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />

<img src="https://img.shields.io/badge/Security-AI%20Agent%20Security-EF4444?style=for-the-badge&logo=shield&logoColor=white" />

</p>

> **What if an MCP tool description itself contains a malicious instruction?**

ToolGate is a security scanner and runtime policy gateway designed to protect AI agents from:

- Tool poisoning
- Prompt injection
- Over-privileged tools
- Dangerous tool arguments
- Secret leakage
- Unsafe tool execution

### Architecture

```text
                    ┌───────────────────┐
                    │     AI AGENT      │
                    └─────────┬─────────┘
                              │
                         JSON-RPC
                              │
                              ▼
                    ┌───────────────────┐
                    │     TOOLGATE      │
                    │   Security Proxy  │
                    └─────────┬─────────┘
                              │
              ┌───────────────┼───────────────┐
              │               │               │
              ▼               ▼               ▼
        ┌──────────┐    ┌────────────┐   ┌────────────┐
        │  Scan    │    │  Policy    │   │  Secrets   │
        │  Tools   │    │  Engine    │   │ Redaction  │
        └──────────┘    └────────────┘   └────────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │    Audit Log      │
                    │     SHA-256       │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │    MCP SERVER     │
                    └───────────────────┘
```

### Core Capabilities

| Capability | What it does |
|---|---|
| 🔍 Tool Scanner | Grades MCP tool inventories from 0–100 |
| 🛡️ Policy Engine | Allow / deny / monitor `tools/call` requests |
| 🔐 Secret Redaction | Recursively removes sensitive values |
| 🧾 Audit Logging | Concurrent-safe JSONL logging |
| #️⃣ SHA-256 Hashing | Avoids storing raw request payloads |
| 📊 Prometheus | Exposes runtime metrics |
| 🚨 Security Checks | Path traversal, shell injection, cloud metadata |
| ⚡ Go | Lightweight concurrent proxy |

**Repository → [github.com/Kartavyasonar/toolgate](https://github.com/Kartavyasonar/toolgate)**

---

# ☸️ Kubernetes & Open Source

### Kubernetes Contributions

#### [PR #138993](https://github.com/kubernetes/kubernetes/pull/138993)

**Rootless namespace testing**

Added `RunInUserNS()` to re-execute test binaries inside unprivileged Linux user and network namespaces, enabling rootless kube-proxy nftables testing.

#### [PR #37058](https://github.com/kubernetes/test-infra/pull/37058)

**Prow CI infrastructure**

Added presubmit CI jobs gated by custom build tags for namespace isolation tests.

#### [Issue #139170](https://github.com/kubernetes/kubernetes/issues/139170)

**ConfigMap BinaryData behavior**

Documented API behavior around `ConfigMap.BinaryData` propagation and validated the behavior with Kubernetes API reviewers.

---

# 🚀 Engineering Work

<details>
<summary><b>⚡ PulseAPI — Distributed API Gateway</b></summary>

### Stack

`Node.js` `Redis` `Kafka` `PostgreSQL` `Prometheus` `Grafana` `k6`

Production-grade API gateway designed for high-concurrency traffic.

### Engineering

- Redis Lua scripts for atomic token bucket rate limiting
- Sliding-window rate limiting
- Distributed circuit breaker state
- Kafka-based asynchronous logging
- PostgreSQL batch writes
- Automatic Grafana provisioning
- Prometheus latency metrics
- Event-loop monitoring

### Load Test

```text
Virtual Users       : 200
Throughput          : 207 req/s
p99 Latency         : 881 ms
Error Rate          : 0.0%
Kafka Batch         : 500 records/sec
```

</details>

---

<details>
<summary><b>🧠 GhostMind — Self-Improving Research Agent</b></summary>

### Stack

`Python` `FastAPI` `FAISS` `NetworkX` `GraphRAG`

LLM-powered research system that learns from retrieval failures using episodic memory and TD learning without retraining model weights.

### Architecture

```text
                    User Query
                         │
                         ▼
                 ┌──────────────┐
                 │ Query Engine │
                 └──────┬───────┘
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
        ┌───────────┐       ┌────────────┐
        │   FAISS   │       │ Citation   │
        │ Vector DB │       │   Graph    │
        └─────┬─────┘       └─────┬──────┘
              │                   │
              └─────────┬─────────┘
                        ▼
                 ┌──────────────┐
                 │   Agent      │
                 │   Reasoning  │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │   Episodic   │
                 │    Memory    │
                 └──────────────┘
```

### Experimental Results

```text
Response confidence
~60%  ─────────────────►  ~83%

Hallucination rate
~40%  ─────────────────►  ~17%

Controlled sessions
57
```

</details>

---

<details>
<summary><b>🤖 Multi-Agent Code Review Platform</b></summary>

`Python` `LangGraph` `ChromaDB` `AST` `Radon` `SSE`

Four specialized agents:

```text
                    ┌─────────────┐
                    │ Source Code │
                    └──────┬──────┘
                           │
                     Python AST
                           │
                           ▼
                 ┌──────────────────┐
                 │ LangGraph Router │
                 └────────┬─────────┘
                          │
        ┌─────────────────┼─────────────────┐
        ▼                 ▼                 ▼
     🐛 Bug           🔐 Security       ⚡ Performance
        │                 │                 │
        └─────────────────┼─────────────────┘
                          ▼
                       Quality
                          │
                          ▼
                    Final Review
```

Includes function-level AST chunking, static complexity analysis, specialized LLM agents, and real-time SSE progress streaming.

</details>

---

<details>
<summary><b>☁️ FaaS Performance Benchmarking</b></summary>

`Kubernetes` `K3s` `OpenFaaS` `JMeter` `Azure Functions`

Benchmarked managed serverless infrastructure against self-hosted OpenFaaS on K3s.

Focus areas:

- Cold-start latency
- Throughput
- Concurrent execution
- Error rates
- Scaling predictability

</details>

---

# 🧰 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=go,python,ts,cpp,bash,postgres,redis,mongodb,kafka,kubernetes,docker,linux,git,github,githubactions,nginx,grafana,prometheus,fastapi,nodejs&perline=7" />
</p>

### Languages

`Go` `Python` `TypeScript` `SQL` `Bash` `C++`

### Backend

`FastAPI` `Node.js` `gRPC` `REST` `JSON-RPC` `WebSockets`

### Infrastructure

`Kubernetes` `Docker` `Linux` `Helm` `GitHub Actions` `nginx`

### Data & Messaging

`PostgreSQL` `Redis` `Kafka` `MongoDB` `SQLite`

### Observability

`Prometheus` `Grafana` `OpenTelemetry` `k6`

### AI & Retrieval

`LangGraph` `FAISS` `ChromaDB` `HuggingFace` `NetworkX` `GraphRAG`

---

# 📊 GitHub Analytics

<p align="center">

<img height="180" src="https://github-readme-stats.vercel.app/api?username=Kartavyasonar&show_icons=true&include_all_commits=true&count_private=true&rank_icon=github&hide_border=true&bg_color=00000000&title_color=00ADD8&icon_color=00ADD8&text_color=8B949E" />

<img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kartavyasonar&layout=compact&langs_count=10&hide_border=true&bg_color=00000000&title_color=00ADD8&text_color=8B949E" />

</p>

---

# 🔥 Contribution Streak

<p align="center">

<img src="https://streak-stats.demolab.com?user=Kartavyasonar&hide_border=true&background=00000000&ring=00ADD8&fire=FF6B35&currStreakLabel=00ADD8&sideLabels=8B949E&dates=8B949E" />

</p>

---

# 🏆 GitHub Achievements

<p align="center">

<img src="https://github-profile-trophy.vercel.app/?username=Kartavyasonar&theme=algolia&no-frame=true&no-bg=true&margin-w=8&row=2&column=4" />

</p>

---

# 📈 Contribution Activity

<p align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Kartavyasonar&bg_color=00000000&color=00ADD8&line=00ADD8&point=FFFFFF&area=true&hide_border=true" width="100%" />

</p>

---

# 🐍 Contribution Snake

<p align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Kartavyasonar/Kartavyasonar/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Kartavyasonar/Kartavyasonar/output/github-contribution-grid-snake.svg">
  <img alt="GitHub contribution snake animation" src="https://raw.githubusercontent.com/Kartavyasonar/Kartavyasonar/output/github-contribution-grid-snake.svg">
</picture>

</p>

---

# 📌 Featured Repositories

<p align="center">

<a href="https://github.com/Kartavyasonar/toolgate">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Kartavyasonar&repo=toolgate&theme=transparent&hide_border=true&title_color=00ADD8&icon_color=00ADD8" />
</a>

<a href="https://github.com/Kartavyasonar/PulseAPI">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=Kartavyasonar&repo=PulseAPI&theme=transparent&hide_border=true&title_color=00ADD8&icon_color=00ADD8" />
</a>

</p>

---

# 🧩 Engineering Principles

```text
┌────────────────────────────────────────────────────┐
│                                                    │
│   Correctness  >  Cleverness                       │
│                                                    │
│   Observability  >  Guesswork                      │
│                                                    │
│   Measured Performance  >  Assumptions              │
│                                                    │
│   Simple Boundaries  >  Distributed Complexity     │
│                                                    │
│   Secure Defaults  >  Hope                         │
│                                                    │
└────────────────────────────────────────────────────┘
```

---

# 💻 Problem Solving

<p align="center">

<img src="https://img.shields.io/badge/600%2B-LeetCode%20Problems-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" />

<img src="https://img.shields.io/badge/Focus-Graphs%20%7C%20Trees%20%7C%20Concurrency-00ADD8?style=for-the-badge" />

</p>

---

# 🎯 Current Focus

```text
                    2026
                     │
       ┌─────────────┼─────────────┐
       │             │             │
       ▼             ▼             ▼
   ToolGate      Kubernetes    Distributed
   Security      Open Source    Systems
       │             │             │
       └─────────────┼─────────────┘
                     │
                     ▼
              Platform Engineering
```

### Building toward

- High-performance Go infrastructure
- Cloud-native security
- AI agent infrastructure
- Kubernetes internals
- Distributed systems
- Production observability

---

# 📫 Connect

<p align="center">

<a href="https://github.com/Kartavyasonar">
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="https://linkedin.com/in/kartavya-sonar23">
<img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>

<a href="https://kartavyasonar.github.io/">
<img src="https://img.shields.io/badge/Portfolio-00ADD8?style=for-the-badge&logo=googlechrome&logoColor=white" />
</a>

<a href="mailto:sonarkartavya@gmail.com">
<img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

</p>

---

<p align="center">
  <b>Build systems that scale. Secure systems that matter.</b>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00ADD8,50:161B22,100:0D1117&height=120&section=footer" width="100%"/>
</p>
