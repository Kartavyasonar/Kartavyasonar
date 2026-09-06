<h1 align="center">Kartavya Sonar</h1>
<h3 align="center">Backend & Platform Engineer · Kubernetes Contributor · Go, Python, Distributed Systems</h3>

<p align="center">
  <a href="https://github.com/Kartavyasonar/toolgate"><img src="https://img.shields.io/badge/🛡️_Building-ToolGate_(MCP_Security_Gateway)-00ADD8?style=flat-square" alt="ToolGate"></a>
  <a href="https://github.com/kubernetes/kubernetes/pull/138993"><img src="https://img.shields.io/badge/Kubernetes-Contributor-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="K8s"></a>
  <a href="https://kartavyasonar.github.io/"><img src="https://img.shields.io/badge/Portfolio-kartavyasonar.github.io-FF5722?style=flat-square" alt="Portfolio"></a>
</p>

---

### 👨‍💻 About Me

I build infrastructure that scales, fails gracefully, and can be observed. My engineering focus is on high-throughput data paths, concurrent Go services, cloud-native security, and AI agent infrastructure.

I care about correctness, clean system boundaries, and engineering that holds up under real load. Previously, I eliminated cascading data integrity failures and reduced API latency by 40% in a production FastAPI + PostgreSQL environment.

- 🔭 **Currently building:** [**ToolGate**](https://github.com/Kartavyasonar/toolgate) — An open-source security gateway for MCP (Model Context Protocol) servers.
- 🌱 **Open Source:** Active contributor to `kubernetes/kubernetes` (sig-network, sig-testing). Authored rootless namespace test helpers reviewed by Google and Red Hat maintainers.
- ⚡ **Core Stack:** Go, Python, Kubernetes, PostgreSQL, Redis, Kafka, Prometheus, OpenTelemetry.

---

### 🛡️ Flagship Project: ToolGate

**[ToolGate](https://github.com/Kartavyasonar/toolgate)** is a security scanner and runtime policy gateway for MCP servers, written in Go. It protects AI agents from tool-poisoning, prompt injection, and over-privileged tool execution.

```text
AI Client ──► [ ToolGate Proxy ] ──► MCP Server
                   │
                   ├─► Policy Engine (YAML)
                   ├─► Recursive PII Redaction
                   ├─► JSONL Audit Log (SHA-256)
                   └─► Prometheus Metrics (/metrics)
```

- **Runtime Enforcement:** Intercepts JSON-RPC `tools/call` traffic. Evaluates allow/deny/monitor policies.
- **Security Scanning:** Statically grades MCP server tool inventories (0-100 score, A-F rating).
- **Observability:** Emits Prometheus metrics and concurrent-safe audit logs without leaking raw payloads.

---

### 🏗️ Infrastructure & Open Source

#### `kubernetes/kubernetes`

- **[PR #138993](https://github.com/kubernetes/kubernetes/pull/138993)** (sig-network): Added `RunInUserNS()`, a test helper that re-executes test binaries inside unprivileged Linux user+network namespaces. Enables rootless `kube-proxy` nftables testing. Reviewed and guided by Google (`aojea`, `BenTheElder`) and Intel (`pohly`) maintainers.
- **[PR #37058](https://github.com/kubernetes/test-infra/pull/37058)** (sig-testing): Added Prow presubmit CI jobs gated by custom build tags for namespace isolation tests.
- **[Issue #139170](https://github.com/kubernetes/kubernetes/issues/139170)**: Documented API gaps in `ConfigMap.BinaryData` propagation, validated by Kubernetes API reviewers.

---

### 🚀 Selected Engineering Work

<details>
<summary><b>PulseAPI — Distributed API Gateway</b> <i>(Node.js, Redis, Kafka, Prometheus)</i></summary>

<br>

Built a production-grade API gateway from scratch to handle high-concurrency traffic with strict reliability guarantees.

<br><br>

<b>Architecture Highlights:</b>

<ul>
  <li><b>Rate Limiting:</b> Redis Lua scripts for atomic token bucket and sliding window algorithms (zero race conditions).</li>
  <li><b>Resilience:</b> Shared circuit breaker state across instances. Kafka async logging pipeline decouples gateway latency from Postgres write throughput (batch-inserts 500 recs/sec with fallback).</li>
  <li><b>Observability:</b> 13-panel auto-provisioned Grafana dashboard tracking <code>histogram_quantile(0.99)</code> latency and event loop lag.</li>
  <li><b>Performance:</b> Load tested at 200 VUs via k6: sustained 207 req/s, p99 latency 881ms, 0.0% error rate.</li>
</ul>

</details>

<details>
<summary><b>GhostMind — Self-Improving Agentic Research System</b> <i>(Python, FastAPI, FAISS, NetworkX)</i></summary>

<br>

An LLM-powered research agent that learns from its own retrieval failures using episodic memory and TD learning, without retraining model weights.

<br><br>

<b>Architecture Highlights:</b>

<ul>
  <li><b>Episodic Memory:</b> Updates Q-values for retrieval strategies based on session confidence.</li>
  <li><b>Hybrid Retrieval:</b> Combines FAISS vector search with NetworkX citation graph traversal (GraphRAG).</li>
  <li><b>Results:</b> Across 57 controlled sessions, response confidence improved from ~60% to ~83%, and hallucination rates dropped from ~40% to ~17%.</li>
</ul>

</details>

<details>
<summary><b>Multi-Agent Code Review Platform</b> <i>(Python, LangGraph, ChromaDB)</i></summary>

<br>

Orchestrates four specialized LLM agents (bug, security, quality, performance) via a LangGraph fan-out graph. Uses Python AST for function-boundary chunking and Radon for static cyclomatic complexity analysis before LLM evaluation. Streams real-time agent progress via SSE.

</details>

<details>
<summary><b>FaaS Performance Benchmarking</b> <i>(Kubernetes, K3s, OpenFaaS, JMeter)</i></summary>

<br>

Comparative study of Azure Functions vs. OpenFaaS on self-hosted K3s. Benchmarked cold-start latency and throughput under concurrent load. Confirmed OpenFaaS on K3s offered more predictable scaling (0% error rate at high concurrency) compared to managed serverless spikes.

</details>

---

### 🛠️ Tech Stack

| Category | Technologies |
| :--- | :--- |
| **Languages** | `Go` `Python` `TypeScript` `SQL` `Bash` `C++` |
| **Backend & APIs** | `FastAPI` `Node.js` `gRPC` `REST` `JSON-RPC` `WebSockets` |
| **Infrastructure** | `Kubernetes` `Docker` `Linux` `Helm` `GitHub Actions` `nginx` |
| **Data & Messaging** | `PostgreSQL` `Redis` `Kafka` `MongoDB` `SQLite` |
| **Observability** | `Prometheus` `Grafana` `OpenTelemetry` `k6` |
| **AI / Retrieval** | `LangGraph` `FAISS` `ChromaDB` `HuggingFace` `NetworkX` |

---

### 📊 Stats & Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Kartavyasonar&show_icons=true&theme=transparent&hide_border=true&hide_rank=false" alt="stats" height="180"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kartavyasonar&layout=compact&theme=transparent&hide_border=true" alt="languages" height="180"/>
</p>

<p align="center">
  <i>600+ LeetCode problems solved · Focus on Graphs, Trees, and Concurrency.</i>
</p>

---

<p align="center">
  <a href="https://linkedin.com/in/kartavya-sonar23">LinkedIn</a> •
  <a href="https://kartavyasonar.github.io/">Portfolio</a> •
  <a href="mailto:sonarkartavya@gmail.com">Email</a>
</p>
