# 🧠 Key Differences: Image Classification vs. Object Detection
Feature	Image Classification	Object Detection
What it returns	Just labels (what’s in the image)	Labels + bounding boxes (what & where)
Use Case	High-level image tagging	Precise localisation (e.g., for robotics, counting)
Frameworks	MXNet, TensorFlow	MXNet, TensorFlow
Model choices	MXNet (ResNet-like), TF Hub (ResNet, MobileNet, etc.)	MXNet (SSD), TF Model Garden
Input format	RGB images (e.g., 224x224 for MXNet)	RGB + JSON for annotations (MXNet)
Training options	Full + transfer learning supported	Full + transfer + incremental supported
Inference output	Image → label(s)	Image → list of objects + coords + confidence
Instances (training)	GPU required (P2/P3/G4/G5), multi-GPU supported	Same (heavy training)
Instances (inference)	CPU (e.g., m5) or GPU (P2/P3/G4/G5)	Same

✅ Exam Tip
If it says “where in the image” → it’s Object Detection.
If it just says “what’s in the image” → it’s Image Classification.
