# 🧠 Amazon Bedrock – Exam Essentials

## 🧱 What is Bedrock?

- A **serverless API service** to access and build on **foundation models** (LLMs, image models).
- Offers access to 3rd-party and Amazon models **without managing infrastructure**.

## 🤖 Foundation Models Available

- **Amazon Titan** (built by AWS)
- **Anthropic Claude**
- **Meta LLaMA**
- **Mistral**, **Cohere**, and **Stability AI** (e.g. Stable Diffusion)
- ❌ No OpenAI models (due to MS partnership)

## 🧰 Key Capabilities

- **Text generation**, **embeddings**, **image generation**
- **Fine-tuning** supported (model-dependent)
- Supports:
  - **RAG** (Retrieval-Augmented Generation)
  - **LLM Agents**
  - **Bring Your Own Model (BYOM)**

## 🛠️ API Endpoints

| Endpoint                  | Purpose                                 |
|--------------------------|-----------------------------------------|
| `Bedrock`                | Model deployment, fine-tuning, mgmt     |
| `Bedrock Runtime`        | Inference (e.g. `invoke_model`, `converse`) |
| `Bedrock Agent`          | Manage tools, agents, knowledge bases   |
| `Bedrock Agent Runtime`  | Run agent-based inference (`invoke_agent`) |

> **Streaming** versions return output one token at a time (like ChatGPT).

---

## 🔐 Permissions & Access

- Must use an **IAM user** (not root) with permissions like:
  - `AmazonBedrockFullAccess`
  - `AmazonBedrockReadOnly`
- You must **request access** for most 3rd-party models.
  - Titan models are available immediately.
  - Approval typically takes a few minutes.

---

## 💵 Pricing Notes

- **Billed via AWS** using **3rd-party model pricing**
- Pricing is **not shown** in the access request flow
- Review rates at: [aws.amazon.com/bedrock/pricing](https://aws.amazon.com/bedrock/pricing)

---

## 🧪 Exam Tips

- Bedrock = no infrastructure management, fast prototyping
- Know it supports **RAG**, **agents**, and **foundation model inference**
- Look for scenarios involving LLM APIs + no server management
