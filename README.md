<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B22,100:00ADD8&height=220&section=header&text=KARTAVYA%20SONAR&fontSize=48&fontColor=FFFFFF&fontAlignY=38&desc=Backend%20%7C%20Platform%20%7C%20Cloud-Native%20%7C%20AI%20Security&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2800&pause=900&color=00ADD8&center=true&vCenter=true&width=850&lines=Backend+%26+Platform+Engineer;Go+%7C+Python+%7C+Kubernetes+%7C+Distributed+Systems;Kubernetes+Open+Source+Contributor;Building+InvokeCordon+%E2%80%94+Security+for+AI+Agents;Designing+systems+that+scale%2C+fail+gracefully%2C+and+stay+observable" alt="Typing animation"/>
</p>

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
  <a href="https://github.com/Kartavyasonar?tab=followers">
    <img src="https://img.shields.io/github/followers/Kartavyasonar?style=for-the-badge&logo=github&label=FOLLOWERS" />
  </a>
  <a href="https://github.com/Kartavyasonar?tab=repositories">
    <img src="https://img.shields.io/github/stars/Kartavyasonar?style=for-the-badge&logo=github&label=STARS" />
  </a>
  <a href="https://github.com/Kartavyasonar">
    <img src="https://komarev.com/ghpvc/?username=Kartavyasonar&style=for-the-badge&color=00ADD8&label=PROFILE+VIEWS" />
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

**[InvokeCordon](https://github.com/Kartavyasonar/InvokeCordon)**

An open-source security gateway for MCP servers, written in Go.

It scans MCP tools for security risks and acts as a runtime JSON-RPC policy gateway between AI agents and MCP servers.

### 🌱 Open Source

Active contributor to **[Kubernetes](https://github.com/kubernetes/kubernetes)** with work around rootless namespace testing, kube-proxy testing, Prow CI, and Kubernetes API behavior.

---

# 🛡️ InvokeCordon

<p align="center">

<a href="https://github.com/Kartavyasonar/InvokeCordon">
<img src="https://img.shields.io/badge/InvokeCordon-MCP%20Security%20Gateway-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
</a>

<img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />

<img src="https://img.shields.io/badge/AI%20Security-EF4444?style=for-the-badge&logo=shield&logoColor=white" />

<img src="https://img.shields.io/badge/Open%20Source-181717?style=for-the-badge&logo=github&logoColor=white" />

</p>

> **What if an MCP tool description itself contains a malicious instruction?**

InvokeCordon is a security scanner and runtime policy gateway designed to protect AI agents from:

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
                    │     InvokeCordon      │
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
| 🛡️ Policy Engine | Allow / deny / monitor `tools/call` |
| 🔐 Secret Redaction | Recursively removes sensitive values |
| 🧾 Audit Logging | Concurrent-safe JSONL logging |
| #️⃣ SHA-256 | Avoids storing raw request payloads |
| 📊 Prometheus | Runtime metrics at `/metrics` |
| 🚨 Security Checks | Path traversal, shell injection, cloud metadata |
| ⚡ Go | Lightweight concurrent proxy |

**Repository → [github.com/Kartavyasonar/InvokeCordon](https://github.com/Kartavyasonar/InvokeCordon)**

---

# ☸️ Kubernetes & Open Source

### 🔹 [PR #138993 — Rootless Namespace Testing](https://github.com/kubernetes/kubernetes/pull/138993)

Added `RunInUserNS()` to re-execute test binaries inside unprivileged Linux user and network namespaces, enabling rootless kube-proxy nftables testing.

**Area:** `sig-network` · **Focus:** Linux namespaces · Rootless Kubernetes

### 🔹 [PR #37058 — Prow CI Infrastructure](https://github.com/kubernetes/test-infra/pull/37058)

Added Prow presubmit CI jobs gated by custom build tags for namespace isolation tests.

**Area:** `sig-testing` · **Focus:** CI/CD · Kubernetes Test Infrastructure

### 🔹 [Issue #139170 — ConfigMap BinaryData](https://github.com/kubernetes/kubernetes/issues/139170)

Documented API behavior around `ConfigMap.BinaryData` propagation and validated the behavior with Kubernetes API reviewers.

**Area:** Kubernetes API · **Focus:** ConfigMap behavior

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

### Results

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

Four specialized agents covering:

```text
🐛 Bug
🔐 Security
⚡ Performance
✨ Quality
```

Uses Python AST for function-level chunking, Radon for static complexity analysis, LangGraph for orchestration, and SSE for real-time progress streaming.

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

# 📊 GitHub Snapshot

<p align="center">

<a href="https://github.com/Kartavyasonar?tab=repositories">
<img src="https://img.shields.io/badge/Repositories-View%20All-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="https://github.com/Kartavyasonar?tab=stars">
<img src="https://img.shields.io/badge/Starred%20Projects-View-00ADD8?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="https://github.com/Kartavyasonar?tab=followers">
<img src="https://img.shields.io/badge/Followers-View-2EA44F?style=for-the-badge&logo=github&logoColor=white" />
</a>

</p>

<p align="center">

<img src="https://img.shields.io/github/commit-activity/y/Kartavyasonar/Kartavyasonar?style=for-the-badge&label=COMMITS%20THIS%20YEAR" />

<img src="https://img.shields.io/github/last-commit/Kartavyasonar/Kartavyasonar?style=for-the-badge&label=LAST%20PROFILE%20UPDATE" />

</p>

---

# 🔥 Contribution Streak

<p align="center">

<img src="https://streak-stats.demolab.com?user=Kartavyasonar&hide_border=true&background=00000000&ring=00ADD8&fire=FF6B35&currStreakLabel=00ADD8&sideLabels=8B949E&dates=8B949E" />

</p>

---

# 📈 GitHub Activity

Your GitHub profile already provides the authoritative contribution graph.

<p align="center">

<a href="https://github.com/Kartavyasonar">
<img src="https://img.shields.io/badge/View%20Full%20Contribution%20Graph-Open%20GitHub%20Profile-00ADD8?style=for-the-badge&logo=github&logoColor=white" />
</a>

</p>

<p align="center">

<a href="https://github.com/Kartavyasonar?tab=overview&from=2026-01-01&to=2026-12-31">
<img src="https://img.shields.io/badge/Contribution%20History-View%20on%20GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

</p>

---

# 🏆 Open Source Impact

<p align="center">

<a href="https://github.com/Kartavyasonar/Kartavyasonar">
<img src="https://img.shields.io/badge/Kubernetes-Contributor-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
</a>

<a href="https://github.com/Kartavyasonar/InvokeCordon">
<img src="https://img.shields.io/badge/InvokeCordon-Building-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
</a>

<a href="https://github.com/Kartavyasonar?tab=overview">
<img src="https://img.shields.io/badge/Open%20Source-Active-2EA44F?style=for-the-badge&logo=opensourceinitiative&logoColor=white" />
</a>

</p>

---

# 📌 Featured Projects

<table>
<tr>
<td width="50%">

### 🛡️ InvokeCordon

**MCP Security Gateway**

Go · JSON-RPC · YAML Policies · Prometheus

Security layer for AI agents and MCP servers.

**[View Repository →](https://github.com/Kartavyasonar/InvokeCordon)**

</td>

<td width="50%">

### ⚡ PulseAPI

**Distributed API Gateway**

Node.js · Redis · Kafka · PostgreSQL

High-concurrency API infrastructure with observability and resilience.

**[View Repository →](https://github.com/Kartavyasonar)**

</td>
</tr>

<tr>
<td width="50%">

### 🧠 GhostMind

**Self-Improving Research Agent**

Python · FAISS · NetworkX · GraphRAG

Retrieval system using episodic memory and adaptive strategies.

</td>

<td width="50%">

### 🤖 Multi-Agent Code Review

**AI Code Analysis Platform**

Python · LangGraph · ChromaDB · AST

Specialized agents for bugs, security, quality and performance.

</td>
</tr>
</table>

---

# 💻 Problem Solving

<p align="center">

<img src="https://img.shields.io/badge/600%2B-LeetCode%20Problems-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" />

<img src="https://img.shields.io/badge/Focus-Graphs%20%7C%20Trees%20%7C%20Concurrency-00ADD8?style=for-the-badge" />

</p>

---

# 🧩 Engineering Principles

<p align="center">

<img src="https://img.shields.io/badge/Correctness-Cleverness-00ADD8?style=for-the-badge" />

<img src="https://img.shields.io/badge/Observability-Guesswork-00ADD8?style=for-the-badge" />

<img src="https://img.shields.io/badge/Measured%20Performance-Assumptions-00ADD8?style=for-the-badge" />

<img src="https://img.shields.io/badge/Secure%20Defaults-Hope-EF4444?style=for-the-badge" />

</p>

```text
┌──────────────────────────────────────────────────────┐
│                                                      │
│   Correctness       >       Cleverness               │
│                                                      │
│   Observability     >       Guesswork                │
│                                                      │
│   Measured Speed    >       Assumptions              │
│                                                      │
│   Simple Boundaries >       Complexity               │
│                                                      │
│   Secure Defaults   >       Hope                    │
│                                                      │
└──────────────────────────────────────────────────────┘
```

---

# 🎯 Current Focus

<p align="center">

<img src="https://img.shields.io/badge/Go-Backend%20Infrastructure-00ADD8?style=for-the-badge&logo=go&logoColor=white" />

<img src="https://img.shields.io/badge/Kubernetes-Open%20Source-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />

<img src="https://img.shields.io/badge/AI-Agent%20Security-EF4444?style=for-the-badge&logo=shield&logoColor=white" />

<img src="https://img.shields.io/badge/Distributed-Systems-7C3AED?style=for-the-badge" />

</p>

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
