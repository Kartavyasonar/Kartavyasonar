# Kartavya Sonar

**Software Engineer · Backend & Distributed Systems · Infrastructure**

MSc Advanced Computer Science, University of Leeds (Russell Group) · BTech CSE, GPA 8.24

![Profile Views](https://komarev.com/ghpvc/?username=Kartavyasonar&color=555555&style=flat&label=profile+views)

---

## About

Software engineer focused on backend systems, distributed architectures, and infrastructure reliability. I build things that are observable, fault-tolerant, and designed to scale from async API backends to multi-node monitoring platforms to retrieval-augmented AI systems.

Previously: eliminated cascading data integrity failures and reduced API latency 40% in a production FastAPI + PostgreSQL environment. I care about correctness, clean system boundaries, and engineering that holds up under real load.

Open to backend, infrastructure, and platform engineering roles.

> **Currently:** Contributing to `kubernetes/kubernetes` · Extending NetPulse with distributed tracing · Preparing research preprint for submission

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)

**Infrastructure & Cloud**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat&logo=nginx&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)

**AI / Retrieval**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)

---

## Selected Projects

### [GhostMind](https://github.com/Kartavyasonar/GhostMind)
Distributed LLM backend with multi-provider failover (OpenAI · Anthropic · Gemini · Groq), async retrieval pipeline, episodic memory system, and GraphRAG reasoning layer. Validated across 57 controlled sessions — response confidence improved from ~60% to ~83%, hallucination rate reduced from ~40% to ~17%.

`Python` `FastAPI` `SQLAlchemy async` `PostgreSQL` `Docker` `NetworkX` `sentence-transformers`

```
Providers ──► Failover Router ──► Async Retrieval Pipeline
                                        │
                          ┌─────────────┼─────────────┐
                       FAISS          BM25        GraphRAG
                          └─────────────┼─────────────┘
                                        ▼
                               Episodic Memory Store (PostgreSQL)
                                        ▼
                                  Response + Confidence Score
```

### [NetPulse](https://github.com/Kartavyasonar/NetPulse)
Distributed network monitoring platform deployed across Oracle Cloud (Mumbai + Frankfurt). Concurrent ICMP probing engine built on raw sockets and asyncio — ARP scanning, traceroute analysis, anomaly detection, and local vs. global outage classification. Full Linux stack: nginx · systemd · UFW · iptables · Let's Encrypt.

`Python` `FastAPI` `asyncio` `Scapy` `PostgreSQL` `Docker` `Oracle Cloud`

```
Node (Mumbai) ──┐
                ├──► Aggregator API ──► Anomaly Detector ──► Alert Engine
Node (Frankfurt)┘         │
                     PostgreSQL
                   (metrics store)
```

### [Serverless FaaS Benchmarking](https://github.com/Kartavyasonar/faas-benchmark)
Comparative performance study of Azure Functions vs. OpenFaaS on K3s. Benchmarked cold start latency, throughput under load, and horizontal scaling behavior across workload profiles.

`Kubernetes` `K3s` `OpenFaaS` `Helm` `Docker` `Python` `JMeter`

### [AI Code Review](https://github.com/Kartavyasonar/AI-CODE-REVIEW)
Multi-agent static analysis platform using LangGraph orchestration and ChromaDB semantic retrieval for vulnerability detection, performance analysis, and structured reporting.

`LangGraph` `ChromaDB` `Python`

### [Nyaya AI](https://github.com/Kartavyasonar/nyaya-ai)
Multilingual legal rights assistant with hybrid RAG pipeline, WhatsApp integration, and legal document generation. Built for low-literacy and non-English users.

`RAG` `BM25` `FAISS` `Python` `WhatsApp API`

---

## Open Source & Research

- Contributor to **kubernetes/kubernetes** — [PR #138993](https://github.com/kubernetes/kubernetes/pull/138993): `RunInUserNS()` helper for unprivileged kube-proxy nftables testing
- First-author NLP preprint under peer review — BERTopic, emotion classification, computational social science
- ACL 2025 · NeurIPS 2024 SoLaR Workshop · EMNLP 2024

605 LeetCode problems solved.

---

[Portfolio](https://kartavyasonar.github.io/) · [LinkedIn](https://linkedin.com/in/kartavya-sonar23) · [GitHub](https://github.com/Kartavyasonar)
