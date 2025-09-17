# 📘 Module 06 – OCI Language & Speech Services

---

## 1️⃣ Trainer’s Lesson Notes

**OCI Language (text analytics):**  
Pretrained models (no data science needed) that analyze unstructured text at scale.

- **Language Detection:** ~75 languages (Afrikaans → Welsh).  
- **Named Entity Recognition (NER):** 14 types (person, org, location, date/time, currency, phone, email, etc.).  
- **Sentiment Analysis:** document, **sentence**, and **aspect** level (e.g., “food great / service poor”).  
- **Key Phrase Extraction:** salient topics/ideas.  
- **Text Classification:** up to ~600 categories/subcategories.

**Console demo flow:** Analytics & AI → **Language** → *Text Analytics* → paste text → **Analyze** → see detection, classification, entities with confidence, key phrases, and multi-level sentiment.

---

**OCI Speech (speech-to-text):**  
Converts audio/video (Object Storage) to **timestamped**, punctuated text with **confidence** scores.

- **Languages:** English, Spanish, Portuguese (more rolling out).  
- **Batching:** submit multiple files per job.  
- **Speed:** hours of audio in minutes (chunking & stitching).  
- **Outputs:** JSON and **SRT** (closed captions).  
- **Normalization:** addresses, times, numbers, URLs → readable forms.  
- **Profanity Filtering:** remove / mask / tag.

**Console demo flow:** Analytics & AI → **Speech** → create **Transcription Job** → select bucket/object → run → view normalized transcript + punctuation & confidences.

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **NER** = highlighter pens that tag names, places, dates in text.  
- **Aspect sentiment** = restaurant bill with per-item thumbs-up/down.  
- **Normalization** = spell-checker that also tidies numbers & times.  
- **SRT** = subtitles file your video players understand.

---

## 3️⃣ DevOps Angle (AIOps)

- **Language**: auto-classify & route tickets; extract entities (case IDs, services); redact PII before indexing.  
- **Speech**: transcribe incident bridges; store SRT + JSON for searchable postmortems; feed transcripts into **Language** for sentiment & key phrases.  
- Wire both to **Event** → **Functions** → **Object Storage** for serverless pipelines.

---

## 4️⃣ Exam Focus

- Language capabilities (detect, entities, sentiment levels, key phrases, classification).  
- Speech features (batch, speed via chunking, JSON/SRT outputs, normalization, profanity modes).  
- Console entry points and typical output artifacts.  

---

## 5️⃣ Beyond Certification

- Pair with **RAG**: transcribe → summarize with LLM → index embeddings.  
- Quality loops: spot-check entity precision/recall; measure WER for Speech; track sentiment drift over time.  

---

## 6️⃣ Resume Booster

> “Built an automated pipeline using **OCI Speech** → **OCI Language** to transcribe bridge calls, extract key topics/PII-redact, and publish searchable summaries; reduced incident review time by 40%.”

**Mini-project idea:**  
Bucket trigger → Speech job → JSON → Language analyze → push summary + SRT to a dashboard.

---

## 7️⃣ Fast-Track Notes

- Language: detect / entities (14) / sentiment (doc, sentence, **aspect**) / key phrases / classify (≈600).  
- Speech: fast batch STT, **SRT**, normalization, profanity handling.  
- Both are **managed** APIs; integrate via Console, REST, SDK, CLI.

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo                | Screenshot    | Notes                                      |
|----------------------------|---------------|--------------------------------------------|
| Test                       | mini-test-07  | Status table showing steps & actions       |
| Questions                  | questions     | ✅ Passed with 100%                        |
