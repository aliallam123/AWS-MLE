# 📘 SageMaker Built-in Algorithm: Linear Learner (Exam Revision)

## ✅ Use Cases
- **Regression** (predict numeric values)
- **Classification** (binary + multi-class)

## 📥 Input Format
- Preferred: `RecordIO-Protobuf` (`float32`)
- Also supports: CSV (`1st column = label, rest = features`)
- Input Modes: 
  - `File` (copies full data to instance)
  - `Pipe` (streams from S3 – preferred for large datasets)

## ⚙️ Key Features
- Normalise data (manually or set `normalize_data=true`)
- Shuffle data before training
- Uses **SGD** (supports optimisers like `Adam`, `Adagrad`)
- Trains **multiple models in parallel**, selects best one
- Supports **L1** and **L2** regularisation:
  - `l1`: sparse models (feature selection)
  - `wd`: weight decay (L2)

## 🎛️ Important Hyperparameters
- `learning_rate`
- `mini_batch_size`
- `l1` (L1 regularisation strength)
- `wd` (L2 regularisation / weight decay)
- `balance_multiclass_weights`: balances class importance
- `binary_classifier_model_selection_criteria`: 
  - `precision_at_target_recall` or `recall_at_target_precision`
- `target_precision` / `target_recall`: used with above criteria

## 💻 Instance Type
- Supports CPU & GPU
- Use multiple instances for scale
- ❌ Multiple GPUs **on one machine** do **not** improve performance

## 🧪 Exam Tips
- Best for linear patterns (not curves or complex boundaries)
- Use **Pipe mode** for large datasets
- Always **normalise** + **shuffle** data
