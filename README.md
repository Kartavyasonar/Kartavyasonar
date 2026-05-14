# Kartavya Sonar

**Backend & Infrastructure Engineer · Kubernetes Contributor · Distributed Systems**

MSc Advanced Computer Science, University of Leeds (Russell Group) · BTech CSE, GPA 8.24

---

## About

Backend and infrastructure engineer with hands-on experience in distributed systems, async architectures, and AI infrastructure. Contributing to **kubernetes/kubernetes** — currently working on unprivileged namespace support for kube-proxy nftables testing. Interested in Kubernetes internals, network reconciliation, node lifecycle, and cloud-native reliability engineering.

Previously: reduced API failure rate to zero and cut latency ~40% at production scale (FastAPI + PostgreSQL). Building systems that are observable, fault-tolerant, and designed to fail gracefully.

Open to backend infrastructure, platform engineering, and distributed systems roles.

---

## Open Source

**kubernetes/kubernetes** — [PR #138993](https://github.com/kubernetes/kubernetes/pull/138993)
Introduced `RunInUserNS()` helper enabling kube-proxy nftables unit tests to run in unprivileged Linux user + network namespaces. Reduces CI privilege requirements and improves test portability across constrained environments. Active in infrastructure and networking issue discussions.

---

## Selected Projects

### [GhostMind](https://github.com/Kartavyasonar/ghostmind)
Distributed LLM backend with multi-provider failover (OpenAI · Anthropic · Gemini · Groq), async retrieval pipeline, episodic memory system, and GraphRAG reasoning layer. Validated across 57 controlled sessions — response confidence improved from ~60% to ~83%, hallucination rate reduced from ~40% to ~17%.
`Python` `FastAPI` `SQLAlchemy async` `PostgreSQL` `Docker` `NetworkX` `sentence-transformers`

### [NetPulse](https://github.com/Kartavyasonar/netpulse)
Distributed network monitoring platform deployed across Oracle Cloud Mumbai + Frankfurt. Concurrent ICMP probing engine using raw sockets and asyncio, with ARP scanning, traceroute path analysis, anomaly detection, and local vs. global outage classification. Managed full Linux stack: nginx · systemd · UFW · iptables · Let's Encrypt.
`Python` `FastAPI` `asyncio` `Scapy` `PostgreSQL` `Docker` `Oracle Cloud`

### [Serverless FaaS Benchmarking](https://github.com/Kartavyasonar/faas-benchmark)
Comparative performance analysis of Azure Functions vs. OpenFaaS on Kubernetes (K3s). Benchmarked cold start latency, throughput under load, and horizontal scaling behavior across workload profiles using JMeter.
`Kubernetes` `K3s` `OpenFaaS` `Helm` `Docker` `Python` `JMeter`

### [AI Code Review](https://github.com/Kartavyasonar/ai-code-review)
Multi-agent static analysis platform. LangGraph orchestration with ChromaDB semantic retrieval — vulnerability detection, performance analysis, structured reporting.
`LangGraph` `ChromaDB` `Python`

### [Nyaya AI](https://github.com/Kartavyasonar/nyaya-ai)
Multilingual legal rights assistant with hybrid RAG pipeline, WhatsApp integration, and legal document generation. Built for low-literacy and non-English users.
`RAG` `BM25` `FAISS` `Python` `WhatsApp API`

---

## Technical Stack

**Languages:** Python · Go · TypeScript · SQL · Bash · C++

**Backend:** FastAPI · Node.js · asyncio · SQLAlchemy async · REST APIs

**Infrastructure:** Kubernetes · Docker · Linux · nginx · systemd · CI/CD · GCP · Oracle Cloud

**Networking:** TCP/IP · ICMP · ARP · BGP (FRRouting) · raw sockets · traceroute

**Databases:** PostgreSQL · MongoDB · SQLite · MySQL

**AI Infrastructure:** RAG pipelines · FAISS · BM25 · sentence-transformers · LangChain · LangGraph · ChromaDB · agentic architectures

---

## Research & Conferences

- First-author NLP preprint under peer review — BERTopic topic modelling, emotion classification, retrieval systems, computational social science
- ACL 2025 (virtual) · NeurIPS 2024 SoLaR Workshop · EMNLP 2024

605 LeetCode problems solved.

---

## Links

[Portfolio](https://kartavyasonar.github.io/) · [LinkedIn](https://linkedin.com/in/kartavya-sonar23) · [GitHub](https://github.com/Kartavyasonar)

---

**Pinned repo suggestions:** kubernetes fork → ghostmind → netpulse → faas-benchmark → ai-code-review → nyaya-ai

**Profile tips:**
- Bio: *Backend & Infrastructure Engineer · kubernetes/kubernetes contributor*
- Add topic tags to each repo: `kubernetes` `distributed-systems` `async` `fastapi` `infrastructure`
- Skip GitHub stats widgets — they dilute technical density
- Add a short architecture diagram (even ASCII) to GhostMind and NetPulse READMEs
