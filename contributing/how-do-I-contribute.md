# Contributing to HybridNet Toddler Pretraining Models

Thank you for your interest in contributing! This repository aims to build a growing, community-driven collection of pretrained HybridNet models for toddler and child posture estimation. Your contribution helps improve generalizability across different environments, ages, and recording setups.

---

## What You Can Contribute

### 1. **Fine-Tuned Model Weights**

If you have fine-tuned the provided pretrained models on your own dataset, you can contribute your updated `.pth` files.

### 2. **Documentation Improvements**

Suggestions, clarifications, typo fixes, or improvements to the README or usage instructions.

### 3. **Metadata About Your Dataset**

If you contribute model weights, please include high-level (non-sensitive) information such as:

* Number of annotated frames
* Age group (e.g., 12–36 months)
* Recording environment (lab, home, daycare, etc.)
* Camera setup (number of views, approximate angles)
* Any known limitations of your dataset

No identifiable data about children should ever be uploaded.

---

## How to Submit Your Contribution

### Step 1 — Fork the Repository

Click the **Fork** button on GitHub to create your own copy of the repository.

### Step 2 — Add Your Files

If contributing new or updated models, add them in a new folder under:

```
pretraining-set/Your_Dataset_Name/
```

Include a short `metadata.txt` or `README.md` describing your dataset.

### Step 3 — Commit and Push

```
git add .
git commit -m "Add fine-tuned model from [Your Dataset Name]"
git push
```

### Step 4 — Open a Pull Request

Go to the main repository and click **New Pull Request**.

Please include:

* A description of what you are contributing
* Dataset metadata (non-identifiable)
* The expected improvements or differences compared to the base model

---

## Important Ethical and Privacy Guidelines

Because the goal is to support research with infants, toddlers, and children, please follow these rules:

* **Never upload raw videos or images of children.**
* **Never upload identifiable metadata.**
* **Only share model weights** and non-sensitive descriptions.
* **Do not share any data that violates your institution’s ethics protocols.**

---

## Testing Your Contribution

Before submitting your pull request, make sure:

* The model loads correctly via the HYBRIDNet/JARVIS pipeline.
* The `.pth` file is not corrupted.
* You have followed the correct folder structure.

If you include metrics (not required), please state how they were computed.

---

## Thanks for Contributing

Your contribution strengthens the scientific community’s ability to study early motor development using markerless 3D posture estimation. Together, we can build a more generalizable and accessible toolkit for developmental researchers worldwide.

If you have any questions, feel free to open an issue or reach out!
