# 🎯 YouTube Comment Classifier – MLOps Portfolio Project

This project showcases a full **MLOps workflow** by fine-tuning and deploying a DistilBERT transformer model to classify YouTube comments into emotional struggle categories (e.g., shame, abandonment, dissociation). It demonstrates model development, scalable deployment, automation, and cloud readiness—ideal for real-world ML pipelines.

---

## 🧠 Core Features

- ✅ **Transformer model** (DistilBERT) fine-tuned on real YouTube comments  
- 🔁 **FastAPI-based inference API** with real-time classification  
- 🐳 **Dockerized end-to-end pipeline**: training → serving → deployment  
- ⚙️ **CI/CD with GitHub Actions**: linting, tests, build & deploy checks  
- ☁️ **Cloud-ready**: deployable on AWS/GCP/Kubernetes (via Docker & K3s)  
- 📊 **Extensible with MLflow or Weights & Biases** (future roadmap)  
- 📂 Clear modular structure for scalable iteration and maintenance  

---

## 📁 Project Structure

```
.
├── data/                 # Raw + preprocessed YouTube comment data
├── model/                # Fine-tuned transformer weights & tokenizer
├── src/                  # Inference and preprocessing pipeline
├── serving/              # FastAPI server + API schema
├── scripts/              # Simulated training scripts
├── deploy/               # Cloud deployment (Docker/K8s/Cloud Run)
├── .github/workflows/    # CI/CD pipelines (lint, test, deploy)
├── Dockerfile            # Containerized setup
├── README.md             # This file
```

---

## 🚀 Run Locally (Developer Mode)

1. **Clone the repo**
```bash
git clone https://github.com/yourname/youtube-comment-classifier-mlops.git
cd youtube-comment-classifier-mlops
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Start the FastAPI server**
```bash
uvicorn serving.app:app --reload
```

→ Visit: [http://localhost:8000/docs](http://localhost:8000/docs) for Swagger UI

---

## 🔁 CI/CD Overview

- ✅ **Linting** via `flake8`  
- ✅ **Unit Testing** with `pytest`  
- ✅ **GitHub Actions** for automated build checks + future deployment hooks  
- ✅ Future: Add staging/production split, DVC tracking, and rollout monitoring

---

## 🧪 Inference Example

**Input**
```json
{
  "text": "I keep sabotaging my relationships because I don't feel worthy of love."
}
```

**Output**
```json
{
  "category": "Shame & Self-Worth",
  "confidence": 0.91
}
```

---

## ☁️ Deployment Options

- **Docker**
```bash
docker build -t comment-classifier .
docker run -p 8000:8000 comment-classifier
```

- **Cloud Platforms**: See `/deploy/README.md`  
  - AWS EC2 with Docker  
  - GCP Cloud Run  
  - Kubernetes (via K3s or EKS)

---

## 📈 Future Enhancements

- ⏺ Full training pipeline with **MLflow**, **DVC**, or **Weights & Biases**
- ⏺ Live frontend for in-browser emotional analysis
- ⏺ Support for multi-model routing and model versioning

---

## 🧠 Model Details

- **Base**: `distilbert-base-uncased` from HuggingFace Transformers  
- **Fine-Tuned On**: Labeled YouTube comments using trauma-informed prompt engineering  
- **Target Classes**: Emotional struggles (e.g., Childhood Trauma, Anxiety, Depression, Numbness)

---

## 👤 Author

**Didi Berman** – AI & Automation Engineer  
Expert in marketing automation, full-stack AI tooling, and MLOps pipelines.  
[📎 GitHub](https://github.com/didiberman) | [🌐 Website](https://didiberman.com)

---

## 📌 Why This Matters

This project demonstrates real-world MLOps workflows—from problem definition and data labeling to transformer fine-tuning, containerization, and deployment—exactly what hiring teams look for in practical ML engineering.
