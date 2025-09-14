# 📘 Module 06 – OCI Data Science (ML Services) & AI Infrastructure

---

## 1️⃣ Trainer’s Lesson Notes

**OCI Data Science (ML Services layer):**  
Managed platform to **build, train, deploy, and manage** ML models with Python & open source.

**Core principles:**
- **Accelerated** – ready JupyterLab, Conda envs, compute shapes (CPU/GPU).  
- **Collaborative** – Projects, shared assets, reproducibility, auditability.  
- **Enterprise-grade** – IAM, managed infra, patching, security.

**Key features/terms:**
- **Projects** – team workspaces for notebooks/models/jobs.  
- **Notebook Sessions** – managed JupyterLab with selectable shapes & storage.  
- **Conda Environments** – curated envs; easy install/switch.  
- **ADS SDK** – Accelerated Data Science library (AutoML, explainability, model ops, Object Storage integration).  
- **Model Catalog** – store/track/share models with provenance (Git, scripts/notebooks).  
- **Model Deployments** – managed HTTPS endpoints for realtime inference.  
- **Jobs & Pipelines** – repeatable ML tasks & orchestrations.

**GPU Foundations (why GPUs?):**  
Massively parallel math for training/inference; deep learning libs (TF/PyTorch/ONNX) exploit **Tensor Cores**.

**NVIDIA GPU evolution (high level):**
- **A100 (Ampere, 2020)** → DL acceleration with tensor cores.  
- **H100/H200 (Hopper, 2022/2024)** → Transformer Engine; H200 adds more memory.  
- **B200 / GB200 (Blackwell, 2025)** → next-gen scale for frontier LLMs.  
- **Grace CPU & GB200 superchip** → tight CPU–GPU coupling for AI/HPC.

**OCI AI Infrastructure & Scale:**
- Broad GPU shapes (L40, H100/H200, B200, GB200) & **RDMA Superclusters**.  
- Superclusters deliver **lossless, low-latency (≈6.5–20µs)** Clo-fabric with **RoCE** and **placement/locality hints** to minimize cross-block hops and collisions.

**LLM Quick Actions (OCI Data Science):**
- **Deploy** popular base models to GPU VMs/bare metal.  
- **Fine-tune** and **serve** via managed endpoints (supports vLLM/text-embedding containers).

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **Projects** = team “folders” with notebooks/models.  
- **Model Catalog** = GitHub for trained models (versioned artifacts + metadata).  
- **RDMA Supercluster** = high-speed GPU “city grid” where any GPU talks to any other with minimal traffic jams.

---

## 3️⃣ DevOps Angle (MLOps)

- Reproducible pipelines with **Jobs/Pipelines**; store artifacts in **Model Catalog**.  
- **ADS SDK** to standardize train→verify→save→deploy steps.  
- Infra as Code for **shape selection**; autoscaling endpoints; logs/metrics wired to Observability.  
- Promotion gates: **dev → staging → prod** with drift checks & canaries.

---

## 4️⃣ Exam Focus

- Data Science components (Projects, Notebook Sessions, Conda, ADS, Model Catalog, Deployments, Jobs).  
- What ADS `.prepare() / .verify() / .save() / .deploy()` do.  
- GPU value props; Transformer acceleration; managed infra benefits.  
- Quick Actions for LLMs (deploy/fine-tune/serve).  
- RDMA Supercluster goals: **lossless fabric, QoS buffers, placement/locality hints**.

---

## 5️⃣ Beyond Certification

- Integrate with **Object Storage**, **Functions**, **Events**, **API Gateway**.  
- Model governance: lineage, approvals, automated evals (accuracy, latency, cost).  
- Canary & blue/green for model endpoints; shadow testing.

---

## 6️⃣ Resume Booster

> “Productionized a RandomForest model on **OCI Data Science**: standardized with **ADS** (prepare→verify→save→deploy), registered to **Model Catalog**, and exposed a managed HTTPS endpoint with autoscaling.”

**Mini-project idea:**  
Notebook → ADS workflow → Model Catalog → Deploy → API Gateway front → CloudEvents notify on new versions.

---

## 7️⃣ Fast-Track Notes

- Data Science = managed **build/train/deploy** with Jupyter + ADS.  
- Model Catalog centralizes artifacts & provenance.  
- GPUs (H100/H200/B200/GB200) for DL/LLMs; Quick Actions simplify LLM ops.  
- RDMA Superclusters = **low-latency, lossless** scale with placement hints.

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test / Demo                | Screenshot    | Notes                                      |
|----------------------------|---------------|--------------------------------------------|
| Test                       | mini-test-05  | Status table showing steps & actions       |
| Questions                  | questions     | ✅ Passed with 100%                        |


---

## 🧪 Appendix – The Demo You Described (Iris RF via ADS)

**Flow:** import libs → load iris → split → train `RandomForestClassifier` → `ads.Model().prepare().verify().save()` → (optionally) `deploy()` and `predict()`.

**Why it matters:** shows the **standard ADS lifecycle** and how **Model Catalog** + **Deployments** make MLOps reproducible.
