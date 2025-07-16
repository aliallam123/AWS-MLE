# SageMaker Studio, Debugger, and Model Registry – AWS MLE-A Exam

---

## 🧠 SageMaker Studio (2020 Feature)

- Web-based **IDE** for end-to-end ML in SageMaker
- Integrates Jupyter notebooks with:
  - **Notebook sharing**
  - **Hardware switching (no infra setup)**
- Enables no-code and low-code workflows

### 🎯 Studio Components
| Feature      | Purpose                                         |
|--------------|--------------------------------------------------|
| **Notebooks**     | Shareable, managed on AWS hardware              |
| **Experiments**   | Track, compare, search historical jobs          |

---

## 🧪 SageMaker Debugger

- Captures **model internals** (gradients, tensors) during training
- Allows **real-time monitoring** and **automatic alerts**

### 🔍 Key Capabilities
- Define **rules** to detect conditions (e.g. overfitting, loss spikes)
- Trigger **CloudWatch events**, **SNS notifications**, or **stop training**
- Supports: **TensorFlow**, **PyTorch**, **MXNet**, **XGBoost**

### 🛠️ Integration
| Tool                     | Function                                      |
|--------------------------|-----------------------------------------------|
| **Studio Debugger Dashboard** | Visual insights during training                |
| **SME Debug**            | Python client library for hooks/API access    |
| **Profiler Rules**       | Monitor CPU/GPU, framework bottlenecks        |

---

## 🧾 SageMaker Model Registry

- Central **database-like catalog** for ML models

### 🧩 Core Functions
- Store **model versions + metadata**
- Track **approval status** (e.g. for production deployment)
- Share models across teams/apps
- Integrates with **CI/CD** (EventBridge, Lambda, API Gateway)

### 🧠 Tied to Governance
- Supports **Model Cards**: describe model limitations, training data
- Works with **approval workflows** (manual or automated)

---

## 🧠 Exam Tips

- "Track all past jobs & compare models" → **Experiments**
- "Monitor gradients, stop on failure" → **Debugger rules**
- "Auto-send alert or stop training on anomaly" → **CloudWatch + SNS**
- "Central place to manage model versions + approvals" → **Model Registry**
- "Model card linked to registry" → governance & transparency
