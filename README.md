# Nexledge 🚀
> **Architecting the Next Ledge of Intelligence.**

Nexledge is a high-performance, reactive AI-native platform designed to bridge the gap between raw LLM capabilities and structured professional knowledge. Built with a robust **Monorepo Microservices** architecture, it emphasizes resilience, context persistence, and multi-model orchestration.

---

## 🏛️ High-Level Design (HLD)

Nexledge is engineered for scalability and modularity. By decoupling the AI logic from the core identity and gateway layers, the system ensures high availability and seamless failover.

### **Core System Architecture**
* **API Gateway:** Powered by **Spring Cloud Gateway**. Acts as the entry point for all traffic, managing rate limiting and request routing.
* **Auth Service:** A centralized identity provider utilizing **OAuth 2.0 / OIDC** (Google & GitHub) to ensure secure, stateless authentication.
* **Intelligence Router:** The "AI Brain" built with **Spring AI**. It orchestrates requests across Gemini 1.5, Groq, and Llama, featuring automated failover logic.
* **Memory Service:** An asynchronous worker using **Apache Kafka** to process session streams and store vector embeddings in **PostgreSQL (pgvector)**.
* **Web Dashboard:** A high-speed, signal-driven **Angular 19** interface providing real-time AI streaming and workspace management.

---

## 🛠️ Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Backend** | Java 21, Spring Boot 3.4, Spring AI |
| **Frontend** | Angular 19, Tailwind CSS, RxJS/Signals |
| **Infrastructure** | Docker, Apache Kafka, PostgreSQL (pgvector), MongoDB |
| **Protocols** | REST, gRPC (Internal Service Communication) |
| **DevOps** | GitHub Actions (Selective Build Pipeline) |

---

## ✨ Key Features
* **Event-Driven Context:** Uses Kafka to ensure the AI never "forgets" the middle of a complex conversation.
* **Model Agnostic:** Seamlessly switch between LLM providers to optimize for cost or performance.
* **Long-Term Memory:** RAG-based persistence allows Nexledge to learn user preferences over time.
* **Enterprise Security:** Secure-by-design architecture with encrypted session handling.

---

## 🗺️ Roadmap
- [x] **Phase 0:** Monorepo Shell & Infrastructure (Docker, Postgres, Mongo, Kafka)
- [ ] **Phase 1:** OAuth2 Auth Service & Gateway Implementation
- [ ] **Phase 2:** Reactive AI Streaming UI with Angular 19
- [ ] **Phase 3:** Vector Memory & RAG Integration
- [ ] **Phase 4:** Scholar Module (Document Intelligence & PDF Analysis)

---

## 🚀 Getting Started

### **Prerequisites**
* Docker Desktop (with WSL2 enabled)
* Java 21
* Node.js (LTS)

### **Local Setup**
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/pravudatta10/nexledge.git](https://github.com/pravudatta10/nexledge.git)
