# 📘 Module 05 – OCI AI Services Overview

---

## 1️⃣ Trainer’s Lesson Notes

**What are OCI AI Services?**  
Prebuilt, managed AI APIs that you call with your data—**no infra to manage**. Many are **pre-trained**, and several support **custom training** on your domain data.

**How they fit the stack:**  
Data & infrastructure → **AI/ML services** → applications. AI services consume your data; apps consume the services.

**Ways to access:**
- **OCI Console** (UI) – quick starts, notebooks, service UIs  
- **REST APIs** – full control via HTTP  
- **Language SDKs** – Java, Python, TypeScript/JS, .NET, Go, Ruby  
- **OCI CLI** – scriptable without boilerplate

**Service catalog (high level):**
- **Language** – language detection, sentiment, key phrases, text classification, NER, PII detection; **custom** NER & classification; **translation** (NMT)
- **Vision** – image classification, object detection, OCR; **custom** image classification & custom object detection (with bounding boxes)
- **Speech** – speech-to-text from media; JSON/SRT outputs
- **Document Understanding** – OCR, word/line boxes, **key-value extraction** (receipts/invoices/IDs), **table extraction**, document classification
- **Digital Assistant** – build chat/voice skills; orchestrate multi-skill conversations (greetings, routing, disambiguation, exits)

**Key takeaways:**
- Managed endpoints (no servers).  
- Pretrained gets you started fast; custom models boost accuracy on domain text/images/docs.  
- Uniform access via Console, APIs, SDKs, CLI.

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **AI Services** = “Power outlets” for AI: plug your app in and get intelligence on demand.  
- **Custom models** = “Tailor fit”—same outfit, fitted to your domain.

---

## 3️⃣ DevOps Angle (AIOps)

- **Language**: classify tickets, extract PII, summarize incidents, translate runbooks.  
- **Vision**: parse screenshots of failing dashboards, extract error codes via OCR.  
- **Document Understanding**: auto-ingest invoices/IDs to JSON for finance/KYC pipelines.  
- **Speech**: transcribe war-room calls for searchable postmortems.  
- **Digital Assistant**: front-door bot for CI/CD status, on-call FAQs, runbook shortcuts.

---

## 4️⃣ Exam Focus

- Access methods (Console, REST, SDKs, CLI) & when to use each.  
- Difference between **pretrained** vs **custom** models across Language/Vision/DU.  
- DU capabilities: OCR, key-value, tables, classification.  
- Speech outputs (JSON/SRT).  
- Digital Assistant: skills, routing, interruptions/disambiguation.

---

## 5️⃣ Beyond Certification

- Compare with **AWS** (Comprehend, Rekognition, Transcribe, Textract, Lex) and **GCP** (NL API, Vision, Speech, Document AI, Dialogflow).  
- Add **guardrails** (PII redaction, rate limits) and **observability** (latency, accuracy tracking).

---

## 6️⃣ Resume Booster

> “Built a serverless pipeline on **OCI Language** and **Document Understanding**: auto-classifies tickets, extracts key fields from invoices, and posts JSON to Object Storage—reduced manual effort by 70%.”

**Mini-project idea:**  
Event-driven DU → KV extraction (invoices) → store JSON → notify via Functions.

---

## 7️⃣ Fast-Track Notes

- Managed APIs; **no infra**.  
- **Language/Vision/Speech/DU/Digital Assistant** = core set.  
- **Custom training** where domain accuracy matters.  
- Multiple access paths (Console/REST/SDK/CLI).

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo                | Screenshot    | Notes                                      |
|----------------------------|---------------|--------------------------------------------|
| Test                       | mini-test-05  | Pretrained; doc-level sentiment            |
| Questions                  | questions     | ✅ Passed with 100%                        |

---
