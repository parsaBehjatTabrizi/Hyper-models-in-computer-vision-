# Hyper-models-in-computer-vision-
Using computer vision Hyper-models on Chest X-Ray Images (Pneumonia)
# 🩻 Pneumonia Detection from Chest X-Rays using EfficientNet (Baseline & HyperModel)

## 📌 Project Overview

This project focuses on detecting **Pneumonia** from **Chest X-Ray** images using deep learning techniques. The dataset used is the publicly available **Chest X-Ray Pneumonia** dataset from [Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia), which includes images categorized into **train**, **val**, and **test** folders.

The project is divided into two main parts:
- A **baseline model** using EfficientNet-B0
- A **HyperModel** using EfficientNet-B3 with advanced training enhancements

---

## ✅ Dataset Description

- **Source**: Paul Mooney – Chest X-Ray Pneumonia ([Kaggle link](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia))
- **Classes**: `NORMAL`, `PNEUMONIA`
- **Structure**:
  - `train/`: Used for model training
  - `val/`: Used for validation during training
  - `test/`: Used for final model evaluation

---

## 🧠 Part 1: Baseline Model with EfficientNet-B0

The first model uses a lightweight and efficient CNN, **EfficientNet-B0**, to classify chest X-ray images. It was trained using standard data preprocessing techniques without any complex optimization strategies.

**Key Details**:
- Input size: 224x224
- Optimizer: Adam
- Loss: CrossEntropyLoss
- Trained for 5 epochs
- Evaluated using the separate `test` dataset

**🔍 Result**:  
The baseline EfficientNet-B0 model achieved an **average accuracy of 81.09%** on the test dataset.

---

## 🚀 Part 2: HyperModel with EfficientNet-B3

To improve performance, a more advanced version was built using **EfficientNet-B3**, paired with a range of optimization strategies:

**Enhancements Applied**:
- Advanced **data augmentation** (random flip, rotation)
- **Learning rate scheduler** for adaptive training
- **Early stopping** to prevent overfitting
- **Confusion matrix** and **classification report** for detailed test evaluation
- **EfficientNet-B3** backbone for improved feature extraction

**📈 Result**:  
The HyperModel achieved **higher accuracy** than the baseline model, outperforming the initial 81.09% by a significant margin, while also providing deeper insight into the model's performance across both classes.

---

## 📊 Example Output

```text
Epoch 5: Train Loss=0.2341, Val Loss=0.1890, Val Acc=92.65%

Classification Report:
              precision    recall  f1-score   support
NORMAL           0.91       0.94      0.92       234
PNEUMONIA        0.97       0.94      0.95       390
