# Convolutional Neural Networks (CNNs) – AWS MLE-A Exam

## 🧠 Key Concepts

- **CNNs** detect patterns in data regardless of **location** (feature location invariance).
- Mainly used for **image classification**, but also useful in **NLP tasks** like sentiment or translation.
- Mimics **visual cortex**: builds up from edges → shapes → objects.

## 🔧 Core Keras Layers

| Layer         | Function                                        |
|---------------|--------------------------------------------------|
| Conv2D        | Detects local features in image patches         |
| MaxPooling2D  | Reduces dimensionality by keeping max values    |
| Flatten       | Converts 2D feature maps into 1D input          |
| Dropout       | Reduces overfitting by randomly dropping nodes |
| Dense         | Standard fully connected neural layer           |
| Softmax       | Final classifier for multi-class classification |

## 🔬 Architecture Examples

| Name       | Purpose                          |
|------------|----------------------------------|
| LeNet-5    | Handwriting recognition          |
| AlexNet    | Deeper, general image classifier |
| GoogLeNet  | Uses inception modules           |
| ResNet-50  | Deep net with skip connections – popular in SageMaker |

## ⚠️ Exam Tips

- **Conv1D**: For text data.
- **Conv3D**: For 3D volume data (e.g., medical imaging).
- **ResNet variants** (especially ResNet-50) are common in AWS image pipelines.
- Understand CNN layers' flow: Conv → Pool → Dropout → Flatten → Dense → Softmax.
