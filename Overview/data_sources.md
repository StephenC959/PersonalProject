# 📊 Clean Datasets for Learning CNNs & Transformers (PyTorch / TensorFlow)

## 🎯 Purpose
This document lists **high-quality, pre-cleaned datasets** that allow you to focus on:
- Model building (CNNs, Transformers)
- Training pipelines
- Evaluation

👉 These datasets **require little to no data cleaning**, making them ideal for independent learning outside university.

---

# 🔥 Recommended Datasets (No Cleaning Required)

---

## 1. MNIST (Baseline / Zero Friction)

- 70,000 handwritten digit images  
- Pre-split into train/test  
- Extremely lightweight  

🔗 Source:  
https://365datascience.com/trending/public-datasets-machine-learning/

### Why use it:
- Perfect for learning pipelines
- Fast training (seconds)
- No preprocessing required

---

## 2. Fashion-MNIST (Better than MNIST)

- Same structure as MNIST  
- Clothing images instead of digits  

🔗 Source:  
https://en.wikipedia.org/wiki/Fashion-MNIST

### Why use it:
- Slightly more complex than MNIST  
- Still zero cleaning  
- Good intermediate step

---

## 3. CIFAR-10 (Best for CNN Learning)

- 60,000 color images  
- 10 object classes (cars, dogs, planes, etc.)  

🔗 Source:  
https://en.wikipedia.org/wiki/CIFAR-10

### Why use it:
- Real-world image classification  
- Standard benchmark dataset  
- Perfect for CNN vs Transformer comparison  

👉 **Recommended main dataset for your projects**

---

# 🚨🚨🚨 IMPORTANT DATASET 🚨🚨🚨

## 4. MedMNIST (HIGH PRIORITY)

⚠️⚠️⚠️ **THIS IS EXTREMELY IMPORTANT FOR YOUR GOALS** ⚠️⚠️⚠️

- Preprocessed medical imaging datasets  
- Multiple tasks (binary, multi-class, multi-label)  
- Same size/format as MNIST (easy to use)

🔗 Source:  
https://arxiv.org/abs/2110.14795

### Why this matters for YOU:
- Direct connection to **medical AI (your stated interest)**
- Clean like MNIST but **real-world relevance**
- Perfect for:
  - CNNs
  - Transformers
  - Future grad school projects

👉 This dataset bridges:
**“toy learning” → “real AI application”**

---

## 5. Caltech-101 (Next Step Up)

- ~9,000 images  
- 101 object categories  

🔗 Source:  
https://en.wikipedia.org/wiki/Caltech_101

### Why use it:
- More complex than CIFAR-10  
- Still relatively clean  
- Good transition to real-world datasets

---

# 🧠 Learning Strategy (Highly Recommended)

## Phase 1 – Learn the pipeline
- MNIST  
- Fashion-MNIST  

👉 Focus:
- DataLoader
- Training loop
- Loss + optimization

---

## Phase 2 – Learn CNN performance
- CIFAR-10  

👉 Focus:
- Convolution layers
- Overfitting vs generalization
- Model tuning

---

## Phase 3 – Architecture comparison
- CIFAR-10 (again)

👉 Compare:
- CNN vs Transformer (ViT-lite)

---

## Phase 4 – Real-world relevance
- MedMNIST ⭐  
- Caltech-101  

👉 Focus:
- Generalization
- More complex patterns
- Domain-specific learning

---

# ⚠️ What to Avoid (For Now)

Avoid datasets that require heavy preprocessing:

- Raw Kaggle datasets  
- Web-scraped image collections  
- Unlabeled or poorly labeled data  

🔗 General dataset discussion:  
https://www.dataquest.io/blog/free-datasets-for-projects/

👉 These will slow you down significantly when your goal is learning models.

---

# 🧩 Pro Tip (What Professionals Do)

Use built-in dataset libraries:

## PyTorch:
- `torchvision.datasets`

## TensorFlow:
- `tf.keras.datasets`
- `tensorflow_datasets`

👉 These are:
- standardized  
- clean  
- optimized for training pipelines  

---

# 🚀 Best Dataset for Your Current Goal

👉 **CIFAR-10**

Because:
- Clean
- Realistic
- Fast training
- Perfect for CNN vs Transformer experiments

---

# 🏁 Final Takeaway

You do NOT need to search for datasets right now.

Use:
- MNIST → fundamentals  
- CIFAR-10 → core learning  
- MedMNIST ⭐ → real-world relevance  

👉 Focus your energy on:
- architecture
- training loops
- evaluation
- experimentation

NOT data cleaning.

---