# 🧠 Sign Language Words Recognition ML Model

This repository contains a deep learning model for recognizing **word-level American Sign Language (ASL)** gestures. The model is trained using the **WLASL300** dataset and utilizes preprocessed skeletal/keypoint features to classify sign language words effectively.

---

## 📌 Overview

This model uses deep learning techniques, including **body-part-specific processing and Transformer-based sequence modeling**, to recognize ASL words from keypoint data extracted from sign language videos.

- **Task**: Word-level sign language recognition  
- **Input**: Preprocessed keypoint features (hands, body, face) from sign language videos  
- **Format**: Classification

---

## 📊 Dataset Used

The model is trained on the **WLASL300** subset of the [WLASL Dataset](https://github.com/dxli94/WLASL), a curated dataset for **Word-Level American Sign Language**.

- ~300 common ASL words  
- Multiple signers per word  
- High variability and real-world conditions  
- Ideal for training generalizable word-level gesture classifiers

📎 **Preprocessed WLASL data**: Available on [Kaggle](https://www.kaggle.com/datasets/himanko/preprocessed-data-wlasl/code)

---

## 🧠 Model Architecture

The model saved in `best_model.h5` is a **Transformer-based deep learning model** with the following design:

### ✔ Key Features:
- **Modular body-part feature processing** (hands, pose, face)
- **Positional encoding** for temporal awareness
- **Multi-head self-attention layers**
- **Layer normalization, dropout, and dense classification layers**
- **Output layer**: Softmax for word classification

### 🧩 Components:
- `Input`: Shape = `(batch_size, time_steps, num_features)`
- `TransformerEncoder` layers
- `GlobalAveragePooling1D` for temporal aggregation
- `Dense(softmax)` output for classification over ~300 ASL words

---

## 📁 Files Included

| File Name            | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `best_model.h5`      | Trained deep learning model (Keras HDF5 format)                             |
| `ORD2SIGN.npy`       | Mapping from output indices to ASL word labels                              |
| `feature_labels.npy` | Label vector for training/validation data                                   |
| `train.csv`          | Metadata about training samples (e.g., file names, labels, signer info)     |
| `feature_data.npy`   | 🗃 **Large file** — extracted keypoint features from ASL videos              |

📥 Download `feature_data.npy` (hosted externally due to GitHub size limits):  
👉 [Google Drive – feature_data.npy](https://drive.google.com/)  
**Place it in the same directory as your script or notebook before training/evaluation.**

---
