# 🔍 VisionForge AI

### AI-Powered Industrial Defect Detection & Visual Inspection System

VisionForge AI is a computer vision-based industrial inspection system designed to automate the detection and analysis of manufacturing defects from component images.

The system processes an uploaded inspection image, applies image preprocessing and computer vision techniques, runs an AI/ML model, identifies the defect category, estimates confidence/severity, and generates an inspection result.

> **Project Status:** 🚧 Active Development
> **Application Type:** Industrial AI / Computer Vision / Quality Inspection

---

## 🚀 Overview

Manual visual inspection in manufacturing can be time-consuming and may vary depending on inspection conditions and human judgment.

VisionForge AI explores how computer vision and machine learning can assist industrial quality inspection by automatically analyzing component images.

### Core workflow

```text
Industrial Component Image
            ↓
       Image Upload
            ↓
     Image Validation
            ↓
     Image Preprocessing
            ↓
    Computer Vision / ML
            ↓
     Defect Detection
            ↓
   Classification & Analysis
            ↓
     Severity Assessment
            ↓
      PASS / FAIL Result
            ↓
   Inspection Database
            ↓
      Analytics Dashboard
```

---

## 🎯 Objectives

* Automate image-based industrial inspection
* Detect manufacturing defects using AI
* Classify detected defects
* Analyze defect confidence/severity
* Reduce dependence on manual inspection
* Maintain inspection history
* Provide visual analytics
* Create an extensible architecture for future industrial deployment

---

## ✨ Features

### 🖼️ AI Image Inspection

Upload an industrial component image and process it through the inspection pipeline.

The system performs:

* Image validation
* Image preprocessing
* Defect detection
* Defect classification
* Confidence analysis
* Severity estimation
* Inspection result generation

---

### 🔎 Defect Detection

The system is designed to identify manufacturing defects such as:

* Scratches
* Cracks
* Dents
* Surface abnormalities
* Corrosion
* Contamination
* Deformation
* Missing components

> The actual supported defect classes depend on the dataset and trained model used by the project.

---

### 📊 Inspection Dashboard

The dashboard provides:

* Total inspections
* Passed inspections
* Failed inspections
* Defect distribution
* Recent inspections
* Defect severity
* Confidence scores
* Inspection trends

---

### 📈 Analytics

Visualize:

* Defects by category
* Defects by severity
* PASS/FAIL ratio
* Inspection trends
* Model predictions
* Frequently detected defects

---

### 🗂️ Inspection History

Store previous inspections with:

* Inspection ID
* Component
* Image
* Predicted defect
* Confidence
* Severity
* PASS/FAIL result
* Timestamp

---

### 📤 Dataset / Image Upload

Support image-based inspection and dataset-driven experimentation.

Future versions can support batch inspection and CSV metadata.

---

## 🧠 AI / Machine Learning Pipeline

The computer vision pipeline follows:

```text
Input Image
     ↓
Image Validation
     ↓
Resize / Normalize
     ↓
Image Preprocessing
     ↓
Feature Extraction
     ↓
AI/ML Model
     ↓
Defect Prediction
     ↓
Confidence Score
     ↓
Severity Analysis
     ↓
Inspection Result
```

Depending on the trained model, the system can support:

* Image classification
* Object detection
* Defect localization
* Anomaly detection

---

## 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │   Industrial Image   │
                    └──────────┬───────────┘
                               ↓
                    ┌──────────────────────┐
                    │   React Frontend     │
                    │  Inspection Portal   │
                    └──────────┬───────────┘
                               ↓
                    ┌──────────────────────┐
                    │    FastAPI Backend   │
                    └──────────┬───────────┘
                               ↓
                    ┌──────────────────────┐
                    │ Image Preprocessing  │
                    │ OpenCV / NumPy       │
                    └──────────┬───────────┘
                               ↓
                    ┌──────────────────────┐
                    │   ML / CV Model      │
                    │ Classification /     │
                    │ Object Detection     │
                    └──────────┬───────────┘
                               ↓
                    ┌──────────────────────┐
                    │ Prediction Analysis  │
                    └──────────┬───────────┘
                               ↓
             ┌─────────────────┴─────────────────┐
             ↓                                   ↓
   ┌──────────────────────┐             ┌───────────────────┐
   │ Supabase PostgreSQL  │             │ Analytics Engine  │
   └──────────┬───────────┘             └─────────┬─────────┘
              │                                   │
              └────────────────┬──────────────────┘
                               ↓
                    ┌──────────────────────┐
                    │ Analytics Dashboard  │
                    └──────────────────────┘
```

---

## 🛠️ Technology Stack

### Frontend

* React
* TypeScript
* Vite
* Tailwind CSS
* shadcn/ui
* Recharts
* Lucide React

### Backend

* Python
* FastAPI
* Pydantic
* Uvicorn

### Computer Vision

* OpenCV
* NumPy
* Pillow

### Machine Learning

* Scikit-learn
* PyTorch / TensorFlow
* YOLO, where applicable

### Database

* PostgreSQL
* Supabase

### Development Tools

* Git
* GitHub
* VS Code
* Google Colab

---

## 📁 Project Structure

```text
VisionForge-AI/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── types/
│   │
│   ├── package.json
│   └── README.md
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   │
│   │   ├── api/
│   │   │   ├── inspection.py
│   │   │   ├── analytics.py
│   │   │   └── model.py
│   │   │
│   │   ├── services/
│   │   │   ├── inspection_service.py
│   │   │   ├── preprocessing.py
│   │   │   └── prediction_service.py
│   │   │
│   │   └── ml/
│   │       ├── train.py
│   │       ├── predict.py
│   │       └── preprocessing.py
│   │
│   ├── models/
│   │   └── trained_model/
│   │
│   ├── data/
│   │
│   ├── requirements.txt
│   └── README.md
│
├── database/
│   └── schema.sql
│
├── docs/
│   └── architecture.md
│
├── .env.example
├── .gitignore
└── README.md
```

---

## 🔌 Backend API

The FastAPI backend provides endpoints such as:

### Health

```http
GET /health
```

Checks whether the backend is running.

### Image Inspection

```http
POST /api/v1/inspect
```

Uploads an image and returns the inspection result.

### Inspection History

```http
GET /api/v1/inspections
```

Returns previous inspection records.

### Individual Inspection

```http
GET /api/v1/inspections/{id}
```

Returns detailed information for a specific inspection.

### Analytics

```http
GET /api/v1/analytics
```

Returns inspection and defect statistics.

### Model Status

```http
GET /api/v1/model/status
```

Returns the current model status and version.

---

## 🤖 Model Output

A typical prediction response can contain:

```json
{
  "inspection_id": "INS-0001",
  "defect_class": "SCRATCH",
  "confidence": 0.94,
  "severity": "HIGH",
  "inspection_result": "FAIL",
  "recommendation": "Inspect component surface before further processing."
}
```

The values above are an example response format and are not claimed model results.

---

## 📊 Model Evaluation

When a real model is trained, evaluate it using appropriate metrics.

For classification:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

For object detection:

* Precision
* Recall
* mAP@50
* mAP@50:95

Only report metrics generated from an actual training/evaluation run.

Example:

```text
Model Evaluation
----------------
Accuracy:        [actual value]
Precision:       [actual value]
Recall:          [actual value]
F1 Score:        [actual value]
```

---

## 🗃️ Dataset

The model requires an industrial defect dataset containing images and corresponding labels.

Possible dataset types include:

* Steel surface defect datasets
* Industrial anomaly detection datasets
* Manufacturing inspection datasets
* Custom industrial component datasets

The selected dataset and defect categories should be documented in the project.

> **Important:** Model classes must match the actual dataset used for training. Do not claim support for defect categories that are not present in the trained model.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/VisionForge-AI.git
```

```bash
cd VisionForge-AI
```

---

## 🐍 Backend Setup

Navigate to the backend:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start FastAPI:

```bash
uvicorn app.main:app --reload
```

Backend:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

---

## 💻 Frontend Setup

Open another terminal:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open the URL displayed by Vite.

---

## 🔐 Environment Variables

Create a `.env` file using `.env.example`.

Example:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_key
BACKEND_URL=http://127.0.0.1:8000
```

Never commit real API keys or passwords.

---

## 🧪 Running an Inspection

1. Start the FastAPI backend.
2. Start the React frontend.
3. Open the inspection page.
4. Upload an industrial component image.
5. Backend validates the image.
6. Image preprocessing is performed.
7. The trained model analyzes the image.
8. Defect prediction is generated.
9. Confidence and severity are calculated.
10. Inspection result is stored.
11. Dashboard analytics are updated.

---

## 🔬 Training Pipeline

```text
Dataset
   ↓
Data Validation
   ↓
Image Preprocessing
   ↓
Train / Validation Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Export
   ↓
FastAPI Integration
   ↓
Real-time Inspection
```

The trained model should be versioned and its training configuration documented.

---

## ⚠️ Important Model Transparency

This project distinguishes between:

### REAL ML MODE

A trained model is loaded and produces predictions from actual model inference.

### DEMO MODE

The application UI/API is operating without a trained production model.

Demo results must be explicitly labelled and must not be presented as genuine model predictions.

---

## 🔒 Limitations

This project is a prototype/research-oriented industrial inspection system.

Limitations may include:

* Model performance depends on dataset quality.
* Lighting and camera conditions can affect predictions.
* Defect classes are limited to the training dataset.
* Real manufacturing environments require controlled imaging conditions.
* A production system would require extensive validation.
* Predictions should be verified before being used for critical manufacturing decisions.

---

## 🚀 Future Improvements

* Real-time camera inspection
* Edge-device deployment
* Industrial camera integration
* PLC integration
* Conveyor-belt inspection
* Real-time defect localization
* More industrial defect categories
* Model version management
* Explainable AI
* ONNX/TensorRT optimization
* Edge inference
* Automated inspection reports
* Production monitoring
* MLOps pipeline
* Model drift detection

---

## 🎓 Learning Outcomes

This project demonstrates practical experience in:

* Computer Vision
* Machine Learning
* Deep Learning
* Image preprocessing
* Object detection
* Classification
* REST API development
* FastAPI
* React
* PostgreSQL
* Supabase
* Data analytics
* Model deployment
* Git/GitHub
* Full-stack AI application development

---

## 👨‍💻 Author

**Ayush S**

B.E. Computer Science & Engineering — Artificial Intelligence

Maharaja Institute of Technology, Mysore

---

## ⭐ Project Focus

**Industrial AI • Computer Vision • Automated Inspection • Machine Learning • Predictive Quality Analytics**

---

## 📜 Disclaimer

This project is developed for educational, research, and portfolio purposes.

It is not presented as a certified industrial quality-control system and should not be used for safety-critical manufacturing decisions without appropriate validation.
