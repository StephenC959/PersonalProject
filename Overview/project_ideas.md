# Transformer-Based AI Projects (Graduate-Level Portfolio)

---

## Project 1: CNN vs R-CNN vs Transformer for Object Detection

**Goal:**  
Compare convolutional and transformer-based approaches in object detection tasks.

**Models:**  
- ResNet (CNN baseline)  
- Faster R-CNN  
- DETR (Transformer)  

### Phases:
1. **Data Engineering:**  
   Use COCO dataset, preprocessing, augmentation.

2. **Baseline Models:**  
   Implement CNN + Faster R-CNN.

3. **Transformer Model:**  
   Implement DETR.

4. **Experiments:**  
   - Data efficiency  
   - Occlusion robustness  
   - Generalization  

5. **Deployment:**  
   ONNX export and real-time inference.

### Metrics:
- mAP  
- Latency  
- Training time  
- Robustness  

---

## Project 2: Multimodal Learning (CLIP-style Image-Text Model)

**Goal:**  
Learn joint embeddings between images and text.

**Dataset:**  
- Flickr30k  
- MS COCO captions  

### Phases:
1. **Data Processing:**  
   Clean captions and images.

2. **Model:**  
   - Image encoder (ViT / ResNet)  
   - Text encoder (Transformer)  

3. **Training:**  
   Contrastive learning.

4. **Tasks:**  
   - Image retrieval  
   - Captioning  
   - Zero-shot classification  

5. **UI:**  
   Build simple retrieval interface.

---

## Project 3: Domain-Specific LLM with RAG (Mechanic Assistant)

**Goal:**  
Build a retrieval-augmented chatbot for diagnostics.

**Data:**  
- Manuals  
- Forums  
- Structured documents  

### Phases:
1. **Data Collection + Storage:**  
   MongoDB / FAISS  

2. **Preprocessing:**  
   Chunking, embeddings  

3. **Model:**  
   LLM + RAG pipeline  

4. **Evaluation:**  
   - Task-based evaluation  
   - Human evaluation  

5. **Deployment:**  
   - Chat UI  
   - Optional voice integration  

---

## MedMNIST (HIGH PRIORITY) Summer Project with Sikman

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

UI,
Application (handle services)
System layer(Logic, where build our logic)
Database(MongoDB, usesAWS)