# Words Recognition ML Model

This repository contains a machine learning model designed for recognizing sign language words using preprocessed data and deep learning techniques.

---
The file best_model.h5 is typically used in Keras (a high-level API of TensorFlow) to store a trained deep learning model.
It is a file saved in the HDF5 (Hierarchical Data Format), and it stores a complete Keras model including:

Model architecture:
The structure of the model (layers, connections, etc.), which allows you to reinstantiate the exact same model later.

Trained weights:
All the parameters (weights and biases) the model has learned during training.

## 📊 Dataset Used

✅ This model is trained on the **WLASL300** subset, which is a preprocessed version of the **Word-Level American Sign Language (WLASL)** dataset.  
WLASL300 consists of ~300 common ASL words with multiple signer variations and video samples per word, making it ideal for early-stage gesture classification tasks.

📎 **More info**: [Preprocessed WLASL Data on Kaggle](https://www.kaggle.com/datasets/himanko/preprocessed-data-wlasl/code)


## 📁 Files Included

| File Name            | Description                              |
|----------------------|------------------------------------------|
| `best_model.h5`      | Trained deep learning model (Keras H5 format) |
| `ORD2SIGN.npy`       | Mapping of label indices to sign words   |
| `feature_labels.npy` | Labels corresponding to training data     |
| `train.csv`          | CSV file containing metadata or raw data |

---

## 🚫 Large File (Not on GitHub)

Due to GitHub’s 100MB file limit, `feature_data.npy` is hosted on Google Drive.

📥 **Download it here**:  
[feature_data.npy (Google Drive)](https://drive.google.com/file/d/1HtA5Tzh9UWpD2vHciRLRjjBbvmupN9kZ/view?usp=drive_link)

After downloading, place it in the same directory as your training notebook or script.

---

## 🧠 Model Overview

- Input: `feature_data.npy` – extracted features from videos/images
- Labels: `feature_labels.npy`
- Model: Deep learning (CNN/LSTM or similar)
- Output: Predicted sign language word

---
