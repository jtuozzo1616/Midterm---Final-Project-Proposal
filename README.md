# Midterm---Final-Project-Proposal
📦 **Waste Classification Using Computer Vision**

Course: ITAI 1378 – Computer Vision & AI

Student: José Tuozzo

Project Tier: Tier 1 — Image Classification

Tools: PyTorch, Google Colab, EfficientNet-B0, Grad-CAM

🧠 **Project Overview**

Proper waste sorting plays a crucial role in sustainable environmental management.
However, manual sorting is slow, prone to human error, and leads to contamination in recycling streams.

This project builds a deep-learning based system that classifies waste into six material categories (cardboard, glass, metal, paper, plastic, trash) using a lightweight and efficient CNN architecture.

🎯 Goal: Develop a vision model capable of identifying waste types to support smart recycling systems and reduce waste contamination.

🚨 **Problem Statement**

Recycling facilities struggle with misclassified waste, causing:

Contamination of recyclable material streams

Increased labor cost and processing time

Lower recycling efficiency and environmental impact

Manual sorting is repetitive, tiring, and inconsistent.
A reliable automated solution improves both accuracy and operational efficiency.

💡 **Proposed Solution**

Use a transfer-learning-based CNN to classify waste images and provide real-time predictions for sorting systems.

Key features:

EfficientNet-B0 pre-trained on ImageNet

Fine-tuning on trash classification dataset

Grad-CAM visualizations to verify model attention

Data augmentation to handle real-world variability

⚙️ **Technical Approach**
Component	Choice
Method	Image Classification
Model	EfficientNet-B0
Technique	Transfer Learning
Training	PyTorch + Colab GPU
Explainability	Grad-CAM for heatmaps

Why this model?
EfficientNet-B0 offers strong accuracy-efficiency tradeoff, ideal for student-level hardware while maintaining competitive performance.

🗂 **Dataset Plan**

Dataset: TrashNet-style waste classification dataset

Classes (6): cardboard, glass, metal, paper, plastic, trash

Total images: ~2527

Split: train / validation / test structure

Preprocessing: resize, normalize

Augmentation: flipping, rotation

If dataset access fails → fallback to synthetic + online public waste-classification datasets.

✅ **Success Metrics**

| Metric | Target |
|--------|--------|
| Accuracy | ≥ 90% |
| Per-class Precision / Recall | Balanced across all categories |
| Explainability | Grad-CAM shows correct focus regions |

📅 **Project Timeline**

| Week | Task | Milestone |
|------|------|----------|
| 10 | Dataset preparation & environment setup | ✅ Dataset ready |
| 11 | Model training & fine-tuning | ✅ Working baseline model |
| 12 | Evaluation & improvements | ✅ Achieve accuracy target |
| 13 | Grad-CAM + Demo build | 🎥 System demo ready |
| 14 | Documentation & polish | 📝 Final report |
| 15 | Presentation | 🎯 Final delivery |

⚠️ **Risks & Mitigation**
| Risk | Probability | Mitigation |
|------|------------|-----------|
| Low accuracy | Medium | Data augmentation, adjust LR, freezing strategy |
| Not enough data | High | Use Roboflow / synthetic fallback |
| Overfitting | Medium | Early stopping, dropout |
| Compute limitations | Low | Google Colab GPU, efficient model |


🧰 **Required Resources**

| Resource | Details |
|---------|--------|
| Compute | Google Colab GPU |
| Frameworks | PyTorch, Torchvision |
| Explainability | Grad-CAM |
| Cost | $0 |


### 📂 Repository Structure
Waste-Classification/
│── README.md  ✅ (ya lo tienes)
│── requirements.txt ✅ (lo que te di)
│── notebooks/
│   └── 01_model_training.ipynb ✅ (tu notebook)
│── data/
│   └── README.md ✅ (dataset info)
└── docs/
    └── Mideterm_slides.pdf ✅ (tu PPT exportado a PDF)
    └── README.md ✅ (nota que te di)


🤖 **AI Usage Log**

I used ChatGPT to help refine the written proposal structure and clarify the Grad-CAM explanation.
All model development, code execution, and debugging were performed by me.

🌎 **Expected Impact**

Improves sorting accuracy

Supports sustainability initiatives

Reduces processing waste and contamination

Foundation for future smart recycling bins or robotic sorters

✅ **Quickstart Guide for Running the Project (add to README)**
### 🚀 How to Run

1) Clone the repository

git clone https://github.com/YOUR_USERNAME/Waste-Classification.git
cd Waste-Classification

2) Install dependencies  

3) Open the notebook  

4) Run cells in Google Colab or Jupyter.  

5) Upload dataset when prompted or connect to Roboflow dataset.

✅ Model will train  
✅ Metrics will print  
✅ Grad-CAM heatmaps will show model focus  

