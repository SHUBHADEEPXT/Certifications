# 📘 Module 04 – Generative AI, LLMs & Transformers (with Prompt Engineering)

---

## 1️⃣ Trainer’s Lesson Notes

**What is Generative AI (GenAI)?**  
A subset of deep learning that **creates new content** (text, code, images, audio, video). Models learn underlying patterns in large datasets and generate *new* samples following those patterns (not copies).

**How GenAI differs from traditional ML:**  
- **Traditional ML (supervised):** learns mapping **features → labels**; outputs a label/prediction.  
- **GenAI (pre-training):** learns from **unlabeled, unstructured content**; outputs *new content* (text/image/etc.).  
- (Later) **fine-tuning** can use labeled data for task-specific behavior.

**Types of GenAI models:**  
- **Text-based** (chat, code, articles, Q&A).  
- **Multimodal** (ingest & generate across text, image, audio, video).

**Large Language Models (LLMs):**  
- A **probabilistic model of text**: estimates P(next token | previous tokens).  
- **“Large”** refers to parameter count (hundreds of millions → tens/hundreds of billions).  
- Built on **Transformer** architecture with **self-attention** for long-range context.  
- Capabilities: Q&A, reasoning, summarization, translation, code/gen.

**Transformers (high level):**  
- Overcome RNN limits (vanishing gradients, short context).  
- **Self-attention** lets the model weigh relationships among *all* tokens at once (“bird’s-eye view”).  
- Variants:  
  - **Encoder-only** → understanding/embeddings (RAG, search, classification).  
  - **Decoder-only** → text generation (chat, code, creative writing).  
  - **Encoder–Decoder** → sequence-to-sequence (translation).

**Tokens & Embeddings:**  
- **Tokens**: word/part-word/punctuation units processed by LLMs.  
- **Embeddings**: vector representations capturing semantic meaning (used in **semantic search**, **vector DBs**, **RAG**).

**RAG (Retrieval-Augmented Generation):**  
- Retrieve relevant docs via embeddings → pass to LLM → grounded answer.  
- Reduces hallucinations vs pure zero-shot generation (though not eliminating them).

**Prompt Engineering (intro):**  
- **Prompt** = input text; **prompt engineering** = iteratively shaping prompts for desired behavior.  
- **Instruction tuning** & **RLHF** align models to follow instructions.  
- Useful patterns: **k-shot prompting** (0/1/few-shot), **in-context learning**, **Chain-of-Thought** (reasoning steps).  
- **Hallucinations**: fluent but non-factual outputs; mitigation via retrieval, verification, and careful prompting.

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **GenAI**: Like an art student who studies thousands of paintings, then creates a *new* painting in that style.  
- **LLM**: A super-fast “next-word predictor” that writes sentences one token at a time.  
- **Transformer self-attention**: A discussion moderator who listens to *every* word in the room to understand context.  
- **Embeddings**: Map locations for meaning—words with similar meaning live close together.  
- **RAG**: Open-book exam—first fetch the right pages, then answer.

---

## 3️⃣ DevOps Angle (AIOps)

- **Incident Copilot:** LLMs summarize alerts, correlate logs, draft action items/runbooks.  
- **Knowledge Bot:** RAG over your internal wikis/Confluence/Jira/SOPs for on-call answers.  
- **Change Intelligence:** Summarize PRs, generate release notes, explain diffs.  
- **Infra as Code Assist:** Draft Terraform/Helm/Jenkins snippets from natural language, then review.  
- **Observability:** Use embeddings to cluster similar incidents; use GenAI to generate *hypothesis playbooks*.  

**OCI tie-ins:**  
- **OCI Language/Speech/Vision** for turnkey AI services.  
- **OCI Data Science** for custom training + deployment.  
- **23ai Vector DB + Select AI** for embeddings, semantic search, and RAG pipelines.

---

## 4️⃣ Exam Focus

- **GenAI vs traditional ML** (generation vs prediction; unlabeled pre-training vs labeled training).  
- **LLM basics:** probabilistic next-token prediction; Transformer; parameters ≠ always better performance.  
- **Transformer advantages:** self-attention, long-range dependency handling; encoder/decoder variants.  
- **Tokens & Embeddings:** what they are; why they matter; semantic search.  
- **RAG concept:** retrieval + generation pipeline and why it reduces hallucination.  
- **Prompting patterns:** zero/one/few-shot, in-context, chain-of-thought; role of instruction tuning & RLHF.  
- **Hallucination:** definition, risks, mitigations (retrieval, verification, guardrails).

---

## 5️⃣ Beyond Certification

- **AWS**: Bedrock, SageMaker, Kendra (RAG), OpenSearch vector.  
- **GCP**: Vertex AI, PaLM/Gemini, AlloyDB vector.  
- **OSS**: Hugging Face (Transformers, PEFT, datasets), LangChain/LlamaIndex (RAG), FAISS/Weaviate/Pinecone (vectors).  
- **Enterprise patterns:** policy-aware RAG, evaluation (faithfulness/groundedness), guardrails, prompt versioning, telemetry.

---

## 6️⃣ Resume Booster

**Bullet example:**  
> “Built a **RAG chatbot** on OCI: used 23ai vector DB for embeddings + Select AI for retrieval, and OCI Language for generation to answer on-call SOP queries. Reduced mean time-to-answer by 40%.”

**Mini-project ideas:**  
- **RAG Quickstart**: Markdown docs → embeddings → vector search → OCI Language completion.  
- **Ops Copilot**: Parse Grafana/CloudWatch alerts, summarize likely root cause, propose next actions.  
- **Prompt Pack**: A tested set of prompts (few-shot & CoT) for incident triage, release notes, and postmortems.

---

## 7️⃣ Fast-Track Notes

- **GenAI** = creates; **ML** = predicts labels.  
- **LLM** = next-token prediction using **Transformers** + self-attention.  
- **Tokens/Embeddings** underpin **semantic search** & **RAG**.  
- **RAG** reduces hallucination by grounding on retrieved context.  
- **Prompting**: 0/1/few-shot, in-context, chain-of-thought; **RLHF** for instruction following.

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo            | Screenshot       | Notes                                                                 |
|------------------------|------------------|-----------------------------------------------------------------------|
| GenAI vs ML quiz       | mini-test-04-01  | ❌ Failed - 60%                                                       |
| GenAI vs ML quiz       | mini-test-04-02  | ✅ Passed with 100%                                                   |
| MindMap                | mind-map         | Enitre map of this module                                             |
| Mini-Test-Questions    | questions        | Practice test questions                                               |

---

