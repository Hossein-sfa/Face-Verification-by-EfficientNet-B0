# Face Verification using EfficientNet-B0

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-✔-green)
![Streamlit](https://img.shields.io/badge/Streamlit-✔-red)
![EfficientNet](https://img.shields.io/badge/EfficientNet-B0-purple)

## 🌟 Overview

This project implements **Face Verification (Recognition)** by embedding face features using **EfficientNet-B0**, powered by **FastAPI** as the backend and **Streamlit** as the frontend. It enables fast and accurate face verification by comparing facial embeddings and determining similarity.

## 🚀 Features
- **Face Embedding Extraction** using **EfficientNet-B0**
- **FastAPI Backend** for efficient REST API interaction
- **Streamlit UI** for an interactive interface
- **Face Registration & Verification System**
- **Real-time Processing**
- **Deployable on Local or Cloud Environments**

---

## ⚙️ Tech Stack

- **Model:** [EfficientNet-B0](https://arxiv.org/abs/1905.11946)
- **Backend:** [FastAPI](https://fastapi.tiangolo.com/)
- **Frontend:** [Streamlit](https://streamlit.io/)
- **Deep Learning:** PyTorch, OpenCV
- **Server:** Uvicorn

---

## 📌 Installation

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-repo/face-verification.git
cd face-verification
```

### **3️⃣ Start the FastAPI Backend**
```bash
uvicorn server:app --host 0.0.0.0 --port 8000 --reload
```
- The API will be available at: `http://127.0.0.1:8000`
- Check API Docs at: `http://127.0.0.1:8000/docs`

### **4️⃣ Start the Streamlit Frontend**
```bash
streamlit run app.py
```
- The UI will be available at: `http://localhost:8501`

---

## 📡 API Endpoints

| Method | Endpoint         | Description                   |
|--------|----------------|------------------------------|
| `POST` | `/register/`   | Registers a new face image  |
| `POST` | `/verify/`     | Compares a face for verification |

---

## 🎯 Usage

### **1️⃣ UI Usage (Streamlit)**
1. Run `streamlit run app.py`
2. Navigate to `http://localhost:8501`
3. Choose **Register** to save a face embedding.
4. Choose **Verify** to compare a new face with registered faces.

### **2️⃣ API Usage (FastAPI)**
#### **Register a Face**
```bash
curl -X 'POST' \
  'http://127.0.0.1:8000/register/' \
  -H 'Content-Type: multipart/form-data' \
  -F 'file=@face1.jpg'
```

#### **Verify a Face**
```bash
curl -X 'POST' \
  'http://127.0.0.1:8000/verify/' \
  -H 'Content-Type: multipart/form-data' \
  -F 'file=@face2.jpg'
```

#### **Example Response**
```json
{
  "is_match": true,
  "euclidean_distance": 0.42
}
```

---

## 📊 Model Training (Jupyter Notebook)
The **FaceVerification.ipynb** notebook contains:
- **Dataset Preparation**
- **Training EfficientNet-B0 for Face Embeddings**
- **Evaluating the Model (Accuracy, Precision, Recall, etc.)**
- **Saving the Model for Deployment**

---

## 🛠 Challenges & Innovations
### **Challenges**
- **Handling Variations in Lighting and Angles**
- **Efficient Face Matching with Minimal Latency**
- **Ensuring High Accuracy with Low Computational Cost**

### **Innovations**
✅ **Using EfficientNet-B0** for highly efficient face embeddings.  
✅ **Euclidean Distance-Based Matching** to ensure quick similarity checks.  
✅ **Optimized API with FastAPI & Streamlit** for seamless performance.  

---

## 🤝 Contributing
We welcome contributions! Feel free to **fork** the repo, create a branch, and submit a **pull request**.

---

## 📬 Contact
- **Author:** Hossein Safaei  
- **Email:** hossaf82@gmail.com  
- **GitHub:** [@Hossein-sfa](https://github.com/Hossein-sfa)

---

### 🚀 **Star this repo if you like it!**
