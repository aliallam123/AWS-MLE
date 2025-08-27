# 🧠 Exam-Relevant Differences

| Technique                 | What it Predicts                    | Level of Detail               |
| ------------------------- | ----------------------------------- | ----------------------------- |
| **Image Classification**  | What is in the image                | Whole image                   |
| **Object Detection**      | What + where (bounding boxes)       | Object-level                  |
| **Semantic Segmentation** | What + where (every pixel labelled) | Pixel-level (most detailed) ✅ |


# ✅ What to Remember for the Exam
Returns a segmentation mask (label for each pixel)

Used in medical imaging, robotics, self-driving cars

Supports JPEG/PNG + label maps

Models: FCN, PSPNet, DeepLabV3 (no need to memorise details)

Backbones: ResNet-50, ResNet-101 (pretrained on ImageNet)

Training: GPU only, single machine only

Inference: CPU (c5/m5) or GPU (p3/g4)

# ✅ Quick exam clue:

If the question mentions pixel-level classification → it’s Semantic Segmentation
