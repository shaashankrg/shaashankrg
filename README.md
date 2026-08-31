<h1 align="center">Hi 👋, I'm Shashank</h1>

<p align="center">Sophomore at UT Austin</p>

<p align="center">
  <a href="https://www.linkedin.com/in/shashank-gundreddy-08b105270/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:shashankrg1213@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://YOUR_PORTFOLIO"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/></a>
</p>

---

### Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)

**Backend & Infrastructure**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**AI / ML**

![LlamaIndex](https://img.shields.io/badge/LlamaIndex-8A2BE2?style=flat-square)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Observability & Testing**

![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![JUnit 5](https://img.shields.io/badge/JUnit%205-25A162?style=flat-square&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A6B?style=flat-square&logo=docker&logoColor=white)

---

### Featured Projects

#### 📒 [Ledgerline](https://github.com/shaashankrg/ledgerline)
`Java 21` · `Spring Boot 3.5` · `Apache Kafka` · `PostgreSQL` · `Flyway` · `Kubernetes` · `Helm` · `Prometheus/Grafana` · `Testcontainers`

A payment ledger and reconciliation engine built around how payment systems actually break — tested against real Kafka and Postgres, not mocks.

- Double-entry ledger fed by a 3-broker Kafka cluster, with a reconciliation engine that fuzzy-matches ledger records against settlement files on amount, merchant, and time window
- Survived a 10-minute chaos run: **12,000 transactions, 13 real pod kills, 0 lost or corrupted payments**
- Proved the failure mode it was designed against — Kafka auto-commit dropped **~83% of in-flight payments** when pods were killed mid-batch
- Tests stratified by cost: fast unit tests on every push, chaos and crash-recovery suites nightly against a real `kind` cluster via GitHub Actions
- `make demo` stands up the whole system — Kafka, Postgres, and the observability stack — on a local cluster

#### 🚪 [LLM Gateway](https://github.com/shaashankrg/llm-gateway)
`Python` · `FastAPI` · `Redis` · `Nginx` · `Docker` · `OpenTelemetry` · `Prometheus` · `Grafana`

A multi-provider LLM API gateway built to survive real traffic and real outages.

- Diagnosed and fixed a blocking-Redis event-loop bottleneck to sustain **240 req/s** under concurrent load
- Horizontally scaled behind Nginx (3 replicas) with distributed rate limiting via **atomic Lua scripts** — no race conditions, strict global quotas
- Circuit-breaker state machine for provider outages: **89% success rate** through a simulated 30s outage with verified 5s recovery
- Full-stack tracing of async request lifecycles, validated with chaos and scale tests

#### 📄 RAG Document Extraction Pipeline *(Pfizer Externship)*
`Python` · `LlamaIndex` · `FAISS` · `Tesseract` · `PaddleOCR` · `EasyOCR` · `OpenCV`

Retrieval over regulatory and clinical documents, debugged end to end.

- Rebuilt PDF text extraction to sort by **visual position** instead of content-stream order, taking an eval set from a 36% bottleneck to **100% (14/14)** end-to-end accuracy
- Built a metadata router to bridge the semantic vocabulary gap between regulatory queries and clinical text, closing a 0.004 retrieval gap after ruling out chunking and embedding-model causes
- Benchmarked three OCR engines on synthetically degraded data and patched a silent rotational deskew bug — edge-case match rates went **0% → 78%**

