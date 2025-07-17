# 🧠 TensorBoard + SageMaker – GitHub Revision Notes

## 🧵 Memory Story: "Visualising the Model’s Journey"
Imagine training a model is like watching your plant grow. TensorBoard is the *smart camera*—it shows you how the plant’s height (accuracy/loss) changes daily, reveals how roots (weights) grow deeper, and even maps where each branch (embedding) spreads out in 3D. SageMaker lets you view this camera feed either directly or via a custom link, so you can track and optimise your model’s growth in real time.

---

## 🎯 What You Actually Need to Know for the Exam

- **TensorBoard**:
  - Originally built for **TensorFlow**, now works with **PyTorch** too.
  - Helps **visualise training metrics** (loss, accuracy).
  - Can project **embeddings** from high to low dimensions (2D/3D).
  - Can **view model graphs**, **weight/bias histograms**, and **profile performance**.

- **Integration with SageMaker**:
  - **Fully supported**.
  - Access via **SageMaker Console** or a **web URL** endpoint.
  - Requires **modifying training scripts** slightly (details not tested).

---

## 🧪 Practical Exam Tips

- ✅ **Keyword to watch**: "visualize training", "project embeddings", "profile training"
- ⚠️ **Common distractor**: Assuming TensorBoard is only for TensorFlow. It's compatible with PyTorch too.
- ✅ If a question mentions "**SageMaker + visualisation**" or "**training debugging tools**", **TensorBoard** is likely the right answer.
- 🚫 Don’t waste time memorising script modifications — **not tested**.

---
