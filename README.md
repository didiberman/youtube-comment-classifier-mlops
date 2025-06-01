# 🎯 YouTube Comment Classifier (MLOps Showcase)

This project demonstrates a full MLOps workflow by deploying a pre-trained Transformer model that classifies YouTube comments into emotional struggle categories (e.g., abandonment, shame, fear). It includes data preprocessing, containerized model serving via FastAPI, CI/CD pipelines, and cloud deployment readiness.

---

## 🧠 Project Highlights

- ✅ **Pretrained DistilBERT model** fine-tuned on labeled YouTube comments  
- 🔁 **Automated inference pipeline** using FastAPI  
- 🐳 **Dockerized** for easy deployment and scalability  
- ⚙️ **CI/CD pipeline** using GitHub Actions  
- ☁️ **Cloud deployment-ready** (AWS/GCP/Kubernetes-ready)  
- 📈 Optionally extensible with MLflow or Weights & Biases for experiment tracking  

---

## 📁 Project Structure

```
.
├── data/                 # Raw & preprocessed comments
├── model/                # Pretrained model + tokenizer
├── src/                  # Inference & data pipeline
├── serving/              # FastAPI app & Dockerfile
├── scripts/              # Simulated training, data download
├── notebooks/            # EDA and prototyping
├── deploy/               # Cloud deployment instructions
├── .github/workflows/    # CI/CD pipelines
├── Dockerfile            # Main project Dockerfile
├── README.md             # This file
```

---

## 🚀 How to Run Locally

1. **Clone the repo**

```bash
git clone https://github.com/yourname/youtube-comment-classifier-mlops.git
cd youtube-comment-classifier-mlops
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the FastAPI server**

```bash
uvicorn serving.app:app --reload
```

Then visit `http://localhost:8000/docs` to try the live API!

---

## 🧪 Example Input

```json
{
  "text": "I keep sabotaging my relationships because I don't feel worthy of love."
}
```

**Example Output**

```json
{
  "category": "Shame & Self-Worth",
  "confidence": 0.91
}
```

---

## 🔁 CI/CD

This repo includes:

- ✅ Linting with flake8  
- ✅ Unit testing with pytest  
- ✅ GitHub Actions workflow (`.github/workflows/ci.yml`) to automate quality checks  

---

## ☁️ Deployment Options

- **Docker**:
  ```bash
  docker build -t comment-classifier .
  docker run -p 8000:8000 comment-classifier
  ```

- **Cloud**: See `/deploy/README.md` for guides to deploy on:
  - AWS EC2 with Docker
  - GCP Cloud Run
  - Kubernetes with K3s

---

## 🧠 Model Details

- **Model**: DistilBERT (Hugging Face) fine-tuned on labeled YouTube comments  
- **Categories**: 6–8 emotionally meaningful categories (e.g., abandonment, overwhelm, numbness)  
- **Data**: Labeled by a psychological prompt assistant trained on trauma theory (Thomas Hübl, Gabor Maté, etc.)

---

## 📈 Future Enhancements

- Add full training pipeline with DVC or MLflow  
- Enable multiple model variants (LLMs, small models, distilled)  
- Add frontend for real-time classification  

---

## 👤 Author

**Didi Berman** – AI & Automation Engineer  
Focused on MLOps, AI-powered marketing tools, and scalable automation pipelines.  
[📎 GitHub](https://github.com/didiberman) | [🌐 Website](https://didiberman.com)
