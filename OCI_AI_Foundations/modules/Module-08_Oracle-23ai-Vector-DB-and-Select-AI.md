# 📘 Module 08 – Oracle 23ai Vector DB & Select AI

---

## 1️⃣ Trainer’s Lesson Notes

**23ai + AI Vector Search (built-in):**
- Converged DB supports **relational, JSON, XML, graph, spatial, text, and vectors**.
- New **VECTOR** datatype stores embeddings alongside rows; schema can stay stable as models evolve.
- **VECTOR_EMBEDDING(model, input)** generates embeddings in-DB (or use external API/ONNX models).
- Similarity via **VECTOR_DISTANCE(vec1, vec2, metric)** (cosine default; pick metric per embedding model).
- **Vector Indexes** (INMEMORY NEIGHBOR GRAPH / NEIGHBOR PARTITIONS) speed approximate search; **TARGET ACCURACY** controls quality/latency.
- Works in **SQL joins** (differentiator): run vector search across normalized enterprise data with the optimizer picking the plan.

**Why this matters:** Power semantic search/RAG **directly in SQL** on enterprise data with transactional consistency and security.

**Select AI (Natural Language → SQL):**
- In Autonomous Database, **SELECT AI** lets you “ask in English,” returns results or the generated SQL.
- DB orchestrates: chooses LLM (via **AI Profiles**), engineers prompts from schema metadata, executes SQL safely.
- Pluggable providers (OCI Generative AI, Cohere, OpenAI, Llama, etc.); choose schemas/tables/views per profile.
- Build apps (e.g., APEX) that accept NL queries, show results, and expose **SHOWSQL** for transparency.

**End-to-end pipeline (RAG with 23ai):**
Data loaders → transforms/chunking → **embeddings into VECTOR** columns → **vector search** (top-K) → pass context to LLM → grounded answers.

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **Embeddings** = GPS coordinates of meaning; close = similar.
- **Vector Index TARGET ACCURACY** = a “dial” between speed and precision.
- **Select AI** = a translator who turns plain English into tuned SQL for your schema.

---

## 3️⃣ DevOps Angle (AIOps/Data)

- Keep embeddings **co-located** with business rows → simpler ETL, fewer systems to run.
- Use **SHOWSQL** in Select AI for review hooks; log queries for audit.
- CI/CD: migrate VECTOR columns & indexes with Liquibase/Flyway; test accuracy at multiple **TARGET ACCURACY** settings.

---

## 4️⃣ Exam Focus

- VECTOR datatype, VECTOR_EMBEDDING, VECTOR_DISTANCE (metric choice).
- Vector Index organizations (in-memory vs partitioned) & **TARGET ACCURACY**.
- Joins + vector search in a single SQL query.
- Select AI flow: **SELECT AI …**, AI Profiles, provider choice, **SHOWSQL**.
- Security posture: data stays in tenancy when using OCI GenAI.

---

## 5️⃣ Beyond Certification

- Pair with **LangChain/LlamaIndex** connectors for 23ai.
- Hybrid retrieval: BM25 (text index) **+** vector search rerank.
- Governance: store prompt, SQL, top-K docs, and response for eval & debugging.

---

## 6️⃣ Resume Booster

> “Implemented semantic search on Oracle 23ai: stored document embeddings in **VECTOR** columns, created vector indexes with **TARGET ACCURACY 0.9**, and exposed **Select AI** natural-language analytics in APEX with **SHOWSQL** for transparency.”

**Mini-project idea:**  
Load product manuals → embed → top-K vector search → return sections to LLM → answer user questions (RAG). Add **SHOWSQL** pane and latency/accuracy metrics.

---

## 7️⃣ Fast-Track Notes

- 23ai = converged DB with **built-in vectors** and **SQL similarity**.
- **VECTOR_EMBEDDING**/**VECTOR_DISTANCE** + **Vector Index** = scalable semantic search.
- **Select AI** = NL → SQL with provider pluggability and reviewable queries.

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo                         | Screenshot    | Notes                                               |
|-------------------------------------|---------------|-----------------------------------------------------|
| Practice Test                       | mini-test-06  | Table with VECTOR(dim) alongside relational fields  |
| Questions                           | questions     | ResNet/ONNX or API-based embedding generation       |

---
