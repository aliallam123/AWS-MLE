# 📘 SageMaker Built-in Algorithm: Object Detection (Exam Revision)

## ✅ Overview
- **Type**: Computer Vision – detects objects in images with bounding boxes
- **Use Cases**:
  - Detect and classify **multiple objects** in an image
  - Output includes: **labels**, **bounding boxes**, and **confidence scores**

---

## 🧠 Available Variants
| Variant         | Backend Framework | Models Supported                   |
|----------------|--------------------|-------------------------------------|
| **MXNet**       | CNN + SSD          | `ResNet-50`, `VGG16` (pre-trained on ImageNet) |
| **TensorFlow**  | TensorFlow Garden  | `ResNet`, `MobileNet`, `EfficientNet`, etc.    |

---

## ⚙️ Input Format

### 🔹 MXNet
- **Image formats**: `.jpg`, `.png`
- **Annotations**: JSON format (specify bounding boxes + categories)
- **Supported input**: MXNet RecordIO or image + JSON

### 🔹 TensorFlow
- Format varies depending on selected model (TFRecord, COCO-style, etc.)

---

## 🎛️ Important Hyperparameters

### Common
- `batch_size` / `minibatch_size`
- `learning_rate`
- `optimizer`: standard DL optimizers (Adam, SGD, etc.)

### MXNet-Specific
- Uses data augmentation: `flip`, `rescale`, `jitter`
- Supports:
  - **Transfer learning** (pretrained weights from ImageNet)
  - **Incremental training**

---

## 💻 Instance Support

### Training
- ✅ **GPU required**
- ✅ Supports:
  - Multi-GPU instances
  - Multi-instance training
- Recommended GPU instances:
  - `ml.p2.xlarge`, `ml.p3.2xlarge`
  - Scale up to: `ml.p2.16xlarge`, `ml.p3.16xlarge`
  - Also supported: `ml.g4`, `ml.g5`

### Inference
- ✅ CPU or GPU
- Recommended:
  - CPU: `ml.m5` series
  - GPU: any of `ml.p2`, `ml.p3`, `ml.g4`

---

## 📝 Exam Tips
- **Detects and localises** multiple objects per image
- Outputs: **bounding box**, **class**, **confidence score**
- **MXNet** uses SSD + ResNet or VGG16; input = image + JSON
- **TensorFlow** wraps various pretrained models (via Model Garden)
- Always use **GPU for training**; can use CPU or GPU for inference
