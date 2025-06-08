# 🗂️ Amazon S3 Lifecycle Rules – AWS MLE Exam Notes

## ✅ What Are Lifecycle Rules?
Used to **automate transitions** between S3 storage classes or **expire/delete** objects to save costs.

---

## ⚙️ Key Features

- **Transition**: Move objects to cheaper storage (e.g., S3 Standard ➡️ IA ➡️ Glacier)
- **Expiration**: Auto-delete objects after a set time
- **Noncurrent Version Expiration**: Delete older versions of versioned objects
- **Abort Incomplete Multipart Uploads**: Saves cost from unfinished uploads

---

## 🧠 Rule Triggers

- Based on **object age in days**
- Can apply filters:
  - **Prefix** (e.g., `logs/`)
  - **Tag-based** (e.g., `env=archive`)

---

## 📦 Common Use Cases

| Use Case                        | Lifecycle Action                        |
|----------------------------------|------------------------------------------|
| Archive data after 30 days      | Transition to **S3 Standard-IA**         |
| Deep freeze after 90 days       | Transition to **S3 Glacier Deep Archive**|
| Delete unused logs after 180d   | **Expire** object                        |
| Remove old versions after 7d    | **Noncurrent version expiration**        |

---

## 🛑 Exam Tips

- Lifecycle rules work **only on new objects** from when the rule is added.
- Must have **versioning enabled** for noncurrent version actions.
- Lifecycle rules help with **cost optimisation** (a big exam theme).
- Use **filters** to scope rules to specific objects.
