# Vision Transformer (ViT) – Mango Leaf Disease Classification

## Overview

This project implements a Vision Transformer (ViT) from scratch using TensorFlow/Keras for mango leaf disease classification across 9 classes.

The objective is to evaluate Transformer-based architectures in agricultural image classification and compare their performance with conventional CNN models.

The final model achieved 96% test accuracy on 4,111 images.

---

## Model Architecture

The Vision Transformer was implemented without using pretrained backbones.

Main components:

- Patch extraction using `tf.image.extract_patches`
- Linear patch embedding (Dense projection)
- Learnable positional embeddings
- Multi-Head Self Attention
- Residual connections with Layer Normalization
- MLP classification head with Softmax output

The implementation focuses on understanding the internal structure and training behavior of Transformer-based vision models.

---

## Dataset

- Total images: 4,111
- Number of classes: 9 (8 disease categories and 1 normal class)
- Data sources:
  - MangoLeafBD dataset
  - Self-collected images in Vietnam
- Train / Validation / Test split: 70% / 15% / 15%

Data augmentation:

- Random horizontal/vertical flip
- Random rotation
- Random zoom
- Normalization

---

## Training Configuration

- Optimizer: AdamW
- Learning rate scheduling: Exponential decay
- Loss function: Sparse Categorical Crossentropy
- Regularization: EarlyStopping and ModelCheckpoint
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix

---

## Results

| Model        | Test Accuracy |
|--------------|--------------|
| VGG-16       | 73%          |
| EfficientNet | 75.6%        |
| Custom ViT   | 96%          |

The ViT model demonstrated improved classification performance compared to the CNN baselines under the same dataset conditions.

---

## Technology Stack

- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn

---

## Project Context

This project was developed as part of an academic study focused on applying Transformer architectures to agricultural disease detection.

The work emphasizes model implementation, experimental comparison, and evaluation methodology.
