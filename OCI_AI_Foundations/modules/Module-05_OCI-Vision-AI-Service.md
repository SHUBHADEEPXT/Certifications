# 📘 Module 05 – OCI Vision AI Service (Image Analysis & Document AI)

---

## 1️⃣ Trainer’s Lesson Notes

**Image Analysis (photographic images):**
- **Object Detection:** bounding boxes + labels + confidence; also extracts scene text (signs, plates).  
- **Image Classification:** scene/object tags (e.g., skyscraper, bridge, boat).  
- **Custom Models:** retrain with your images to detect domain-specific objects.

**Document AI (docs & scans: PDF/JPG/PNG/TIFF/handwriting/tilted/rotated):**
- **OCR:** robust text recognition.  
- **Document Classification:** 10 types (invoice, receipt, resume, etc.).  
- **Language Detection:** based on visual features.  
- **Table Extraction:** structured rows/cols.  
- **Key-Value Extraction (receipts):** merchant, date/time, totals, line items.

**Console demo flow:** Analytics & AI → **Vision** → *Image Classification/Object Detection* → test default images or upload → see tags, boxes, and extracted text.  
Document AI → upload receipt/invoice → view raw text, keys, and table extraction.

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **Object Detection** = sticky notes on each thing in a photo.  
- **Document AI** = a diligent clerk who reads receipts, tables, and stamps—even when skewed.

---

## 3️⃣ DevOps Angle (AIOps)

- Parse dashboard screenshots for error codes via **Object Detection + OCR**.  
- Expense/KYC pipeline: **Document AI** → KV + tables → JSON → finance system.  
- Train **custom detectors** for domain items (rack labels, device types, antenna dishes).

---

## 4️⃣ Exam Focus

- Difference: **Classification** (whole-image tags) vs **Detection** (boxes).  
- Document AI features: OCR, doc-type classification, language detect, **KV**, **tables**.  
- When to use **custom** models vs pretrained.

---

## 5️⃣ Beyond Certification

- Combine with **Language** for text understanding post-OCR.  
- Active learning loop: review low-confidence boxes/keys → add to custom dataset → retrain.

---

## 6️⃣ Resume Booster

> “Built a receipt-to-JSON pipeline on **OCI Vision Document AI** extracting merchant/date/line items; auto-reconciled expenses with <2% manual review.”

**Mini-project idea:**  
Upload invoices → Document AI tables → post to Object Storage → trigger Function to validate totals & VAT.

---

## 7️⃣ Fast-Track Notes

- Vision = **Classification + Detection + OCR** (+ custom).  
- Document AI = **OCR + doc-type + language + KV + tables**.  
- Great for expense automation & screenshot parsing.

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo                | Screenshot    | Notes                                      |
|----------------------------|---------------|--------------------------------------------|
| Test                       | mini-test-07  | Pretrained; doc-level sentiment            |
| Questions                  | questions     | ✅ Passed with 100%                        |
