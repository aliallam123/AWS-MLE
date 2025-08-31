# 📘 SageMaker Built-in Algorithm: DeepAR (Exam Revision)

## ✅ Overview
- **Type**: Recurrent Neural Network (RNN) for time series forecasting
- **Use Cases**:
  - Predicting future values of a time series (e.g. stock prices, demand)
  - Forecasting multiple **related** time series
- **Key Feature**: Learns seasonality, trends, and patterns across time

---

## 📥 Input Format
- Formats supported:
  - `JSON Lines` (`.json` or `.json.gz`)
  - `Parquet` (preferred for performance)
- Each record must contain:
  - `start`: timestamp
  - `target`: array of values
  - Optional: `cat` (categorical features), `dynamic_feat` (time-dependent external data)
- Always use **entire time series** (train/test/predict)

---

## ⚙️ Key Features
- Can model **multiple related time series**
- Can ingest categorical and dynamic features
- **Prediction length limit**: ~400 points (avoid longer horizons)
- Uses full historical context to capture seasonality (lags up to 1 year)

---

## 🎛️ Important Hyperparameters

### 🔹 Model/Training
- `epochs`: number of training cycles
- `batch_size`
- `learning_rate`
- `num_cells`: number of RNN units (neurons)
- `context_length`: length of input time window before prediction

### 🔹 Notes
- Choose `context_length` carefully (can be shorter than seasonality)
- **Training requires full time series**, not just recent windows

---

## 💻 Instance Support

### Training
- ✅ Supports CPU & GPU
- ✅ Scales to multi-instance clusters
- ✅ AWS recommends starting with:
  - `ml.c4.2xlarge` (default)
  - `ml.c4.4xlarge` (if more compute needed)
- Use GPU **only** for large models or `batch_size > 512`

### Inference
- ✅ CPU only

### Tuning
- Tuning jobs may require larger/more powerful instances

---

## 📝 Exam Tips
- **Use for time series prediction**
- **Supports multiple related time series**
- Input must include: `start`, `target`, optional `cat`, `dynamic_feat`
- Avoid long prediction lengths (>400)
- Start with **CPU**; use **GPU** only for large-scale training
- Remember `context_length` affects how far back the model looks
