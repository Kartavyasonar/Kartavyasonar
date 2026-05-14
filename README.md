# Hi, I'm Kartavya 👋

### Backend & Infrastructure Engineer | Kubernetes Contributor | Distributed Systems & AI Infrastructure

I build distributed backend systems, cloud-native infrastructure, and intelligent AI platforms focused on reliability, scalability, and real-world engineering tradeoffs.

Currently exploring:

* Kubernetes internals & infrastructure automation
* Distributed systems & observability
* Fault-tolerant AI infrastructure
* Backend performance engineering
* Retrieval & agentic architectures

---

## 🚀 Open Source

### Kubernetes Contributor

Contributing to `kubernetes/kubernetes`.

* Opened PR #138993 introducing a `RunInUserNS()` helper enabling kube-proxy nftables tests inside unprivileged Linux user + network namespaces
* Exploring node lifecycle, reconciliation patterns, networking, and infrastructure workflows
* Active in Kubernetes issue discussions around declarative infrastructure operations

---

## ⚙️ Featured Projects

### GhostMind — Distributed LLM Infrastructure & Agentic Research Backend

**Tech:** Python, FastAPI, SQLAlchemy async, PostgreSQL, SQLite, Docker, React, NetworkX

* Built a distributed multi-provider LLM backend with automatic failover across OpenAI, Anthropic, Gemini, and Groq
* Engineered async retrieval and memory pipelines using episodic RL-inspired memory (MemRL + TD learning)
* Implemented adaptive retrieval strategy selection and GraphRAG-based reasoning
* Controlled 57-session evaluation demonstrated:

  * confidence improvement from ~60% → ~83%
  * hallucination reduction from ~40% → ~17%
* Dockerised deployment with versioned REST APIs and environment-based configuration

---

### NetPulse — Distributed Network Operations & Monitoring Platform

**Tech:** Python, FastAPI, asyncio, PostgreSQL, Scapy, Docker, Oracle Cloud VPS

* Built a geographically distributed network monitoring platform across Oracle Cloud Mumbai + Frankfurt
* Developed concurrent ICMP probing engine using raw sockets + asyncio
* Implemented ARP discovery, traceroute path analysis, anomaly detection, and automated alerting
* Architected failure classification capable of distinguishing local vs. global outages
* Managed full Linux infrastructure stack:

  * SSH hardening
  * nginx reverse proxy
  * systemd services
  * UFW/iptables
  * TLS with Let's Encrypt

---

### Serverless FaaS Benchmarking

**Tech:** Kubernetes (K3s), OpenFaaS, Azure Functions, Helm, Docker, Python, JMeter

* Benchmarked Azure Functions vs OpenFaaS under ML inference workloads
* Evaluated latency, throughput, cold-start behaviour, and scaling characteristics
* Built reproducible cloud-native deployment pipelines using Helm + Docker

---

### AI-CODE-REVIEW

**Tech:** FastAPI, LangGraph, ChromaDB, React, Groq LLaMA 3

* Multi-agent AI system for repository analysis and code reasoning
* Semantic retrieval pipeline for vulnerability and performance analysis
* Structured severity-based reporting grounded in retrieved repository context

---

## 🛠 Technical Areas

### Backend & Infrastructure

* FastAPI
* Node.js / Express
* PostgreSQL / SQLite / MongoDB
* Docker & Docker Compose
* Linux / nginx / systemd
* CI/CD & cloud deployments

### Distributed Systems & Networking

* asyncio
* Concurrent programming
* Fault tolerance & failover
* TCP/IP, ICMP, ARP
* BGP (FRRouting)
* Raw sockets & network diagnostics

### AI Infrastructure

* RAG Pipelines
* Vector Retrieval
* FAISS / BM25
* LangGraph / LangChain
* Embedding systems
* Agentic architectures

---

## 📚 Research

MSc Advanced Computer Science (Merit) — University of Leeds.

Research focused on:

* NLP pipelines
* computational social science
* BERTopic topic modelling
* emotion classification
* retrieval systems
* agentic AI architectures

First-author NLP research preprint currently under peer review.

---

## 🌐 Connect

* Portfolio: https://kartavyasonar.github.io/
* LinkedIn: https://linkedin.com/in/kartavya-sonar23

---

> Building scalable infrastructure and intelligent systems one layer at a time.
