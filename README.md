Rất tốt 👌 mình sẽ viết cho bạn **một phiên bản README gọn – mạnh – đúng thực tế – không phóng đại – không dài dòng**.

Bạn có thể copy nguyên phần này vào repo `Vit-classification`.

---

# 🌿 Vision Transformer (ViT) – Mango Leaf Disease Classification

## 📌 Overview

This project implements a **Vision Transformer (ViT) from scratch using TensorFlow/Keras** to classify mango leaf diseases across **9 classes**.

The goal is to explore how Transformer-based architectures perform in agricultural image classification compared to traditional CNN models.

The model achieved:

> 🎯 **96% Test Accuracy** on 4,111 images
> 🚀 Outperformed VGG-16 and EfficientNet baselines

---

## 🧠 Model Architecture

The Vision Transformer was manually implemented (no pretrained backbone):

* Patch extraction using `tf.image.extract_patches`
* Learnable patch embedding (Dense projection)
* Positional Embedding
* Multi-Head Self Attention
* Residual connections + Layer Normalization
* MLP classification head (Softmax)

This implementation focuses on understanding the internal mechanics of ViT rather than relying on pretrained models.

---

## 📊 Dataset

* Total images: **4,111**
* Classes: **9** (8 diseases + VN Normal Leaf)
* Data sources:

  * MangoLeafBD dataset
  * Self-collected images in Vietnam
* Train/Val/Test split: 70% / 15% / 15%

Data augmentation applied:

* Random Flip
* Random Rotation
* Random Zoom
* Normalization

---

## ⚙️ Training Setup

* Optimizer: **AdamW**
* Learning rate scheduling: Exponential Decay
* Loss: SparseCategoricalCrossentropy
* EarlyStopping & ModelCheckpoint
* Evaluation: Accuracy, Precision, Recall, F1-score, Confusion Matrix

---

## 📈 Results

| Model          | Test Accuracy |
| -------------- | ------------- |
| VGG-16         | 73%           |
| EfficientNet   | 75.6%         |
| **Custom ViT** | **96%**       |

The Transformer-based architecture demonstrated strong generalization across disease categories and showed improved robustness compared to CNN baselines.

---

## 🛠 Tech Stack

* TensorFlow / Keras
* NumPy
* Matplotlib
* Scikit-learn

---

## 🎓 Project Context

This project was developed as part of an academic research study on applying Vision Transformers to agricultural disease detection.

It emphasizes architectural understanding, experimentation, and performance evaluation.

---

✨ Focus: Transformer mechanics • Model experimentation • Real-world dataset application

---

Nếu bạn muốn, mình có thể:

* Viết lại README theo style “AI Engineer Portfolio” chuyên nghiệp hơn nữa
* Hoặc chuyển sang phân tích project AI-capstone để đồng bộ level toàn bộ GitHub của bạn 🔥
