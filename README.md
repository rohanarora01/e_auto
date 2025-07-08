# 🚘 eAuto CV – AI-Powered Carwash Customer Intelligence

## 📌 Project Summary

**Electric Automobiles Limited** is building a unified vehicle service experience through its auto shop, mechanic, gas station, and carwash—all on-site. Their vision is to evolve into a one-stop destination for vehicle owners. As part of their digital transformation journey, they are exploring the use of **AI and Computer Vision (CV)** to understand and engage their customer base better.

This is **eAuto’s first AI Proof-of-Concept (POC)**: a **computer vision pipeline to identify car brands and collect demographic information** of customers using the automated carwash service. The goal is to profile the user base and leverage that data to market other services—especially the auto shop.

---

## 🎯 Objective

Develop a CV system that:

- 📸 **Detects and classifies** the car brand from an image or video feed at the carwash entry.
- 🧑‍🦱 **Estimates customer demographic information** (e.g., age, gender) from visible faces in the image.
- 📊 **Aggregates insights** on customer segments using only the carwash service, to target them with relevant offers from the auto shop.

---

## 🧠 AI Tasks

1. **Car Brand Recognition**
   - Detect and classify vehicle logos from front-facing car images.
   - Trained on 9 common car brands in India:
     - Volkswagen, Honda, Suzuki, Hyundai, Tata, Toyota, Ford, Renault, Nissan.

2. **Demographic Detection**
   - Use face detection and demographic estimation models to infer:
     - Gender
     - Age range
     - (Optional) Ethnicity/Emotion estimation if feasible

---

## 🗃️ Dataset

- **Source:** Web-scraped images of car fronts for initial POC.
- **Challenges:** Variance in angle, lighting, image quality due to uncontrolled scraping.
- **Annotation:** Manual labeling for car logos, bounding boxes for faces.
- **Future Plan:** Real-world data collection from cameras mounted at the carwash entrance.

---

## 🛠️ Tech Stack

| Task                        | Tools/Libraries                             |
|-----------------------------|---------------------------------------------|
| Car Logo Detection          | YOLOv5 / YOLOv8, OpenCV                     |
| Demographic Estimation      | DeepFace / InsightFace / FairFace           |
| Annotation                  | LabelImg / Roboflow                         |
| Backend Pipeline (optional) | Flask / FastAPI                             |
| Visualization               | Streamlit Dashboard (optional)              |

---

## 🧪 Model Pipeline

1. 📷 **Input**: Frame from carwash entrance (real-time or pre-captured).
2. 🧼 **Preprocessing**: Image resizing, normalization.
3. 🚗 **Logo Detection**: Object detection model returns bounding box and car brand.
4. 👤 **Face Detection**: Detect face(s) from driver seat (if visible).
5. 📊 **Demographic Inference**: Run demographic model on detected face.
6. 💾 **Data Storage**: Save anonymized outputs for analysis (brand + demographics).

---

## ⚙️ Getting Started

> _Instructions for development/replication purposes_

### 1. Clone the Repository
```bash
git clone https://github.com/rohanarora01/e_auto_cv.git
cd e_auto_cv
