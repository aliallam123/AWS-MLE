# 📘 SageMaker Built-in Algorithm: PCA (Principal Component Analysis)

## ✅ Overview
- PCA is an **unsupervised** algorithm for **dimensionality reduction**.
- Reduces high-dimensional feature sets into **fewer, unlabelled components**.
- Helps models train faster and avoid overfitting by removing noise and redundancy.

## 🔧 Key Concepts
- **Goal**: Preserve as much variance as possible in fewer dimensions.
- **Used When**:
  - Too many features (curse of dimensionality)
  - You want to simplify input data before modelling

## 🎛️ Key Options (Just the Useful Stuff)
- `algorithm_mode`: 
  - `regular` → default (good for most cases)
  - `randomized` → faster for large/high-dimensional data
- `subtract_mean`: centres data before decomposition (improves accuracy)

## 💻 Instance Type
- Supports **CPU or GPU**
- No strict rule — pick based on data size

## 📝 Exam Tip
> If asked how to simplify or reduce input features, choose **PCA**.  
> You don’t need labels or supervision — just numeric feature data.
