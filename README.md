# 🕵️‍♀️ Image Forgery Detection using PyTorch

This repository contains a PyTorch-based deep learning pipeline for binary image classification:  
- **Classification**: Distinguishing between **Authentic (Au)** and **Tampered (Tp)** digital images.

Dataset used: **CASIA Image Tampering Detection Evaluation Database v2.0**

---

## 🧪 1. Classification Model

### 🔍 Objective  
Classify an input image as either:  
- `Au` → Authentic  
- `Tp` → Tampered

### 📘 Dataset  
We use **CASIA v2.0**, which includes two main folders:  
- `Au/` for original (authentic) images  
- `Tp/` for manipulated (tampered) images  

Each folder is split into `train/` and `test/` sets to facilitate model evaluation.

### 🛠 Preprocessing  
- Images are resized and normalized  
- Augmentations include random flips and rotations  
- Labels are assigned: `0` for Au, `1` for Tp

---

## 🚀 How to Run

### 📦 1. Install Requirements

```bash
pip install -r requirements.txt
```

## 📂 2. Prepare Dataset
Ensure the folder structure is as shown above. Place the Au and Tp images under train/ and test/ directories respectively.
- Au/ → Authentic images
- Tp/ → Tampered images
- Place these images in their respective train/ and test/ directories.

## 🧠 3. Train the Model
```bash
python image-forgery-detector.py.py --mode train --epochs 25 --batch_size 32
```

## 📊 4. Evaluate the Model
```bash
python image-forgery-detector.py --mode test
```

**Note:** The dataset is not included in the repository due to its large size. You can download it from [CASIA v2.0 on Kaggle.](https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset)

## ✅ Results
Accuracy : 88%
Precision : 80%
Recall : 93%
F1 Score : 86%

Model performance was measured on a held-out test set from CASIA v2.0.

## 👨‍💻 Contributors
- Vishwesh Patidar
- Yuvika Yadav

## 🧭 Future Work
- Implement forgery localization using segmentation models
- Test on multi-source datasets (e.g., NIST, Wild, AutoSplice)
- Create a web interface for uploading and verifying image authenticity

## 📜 License
This project is licensed under the MIT License.


