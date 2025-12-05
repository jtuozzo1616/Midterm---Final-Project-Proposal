# Waste Classification Using Computer Vision
Course: ITAI 1378 – Computer Vision & AI
Student: José Tuozzo
Project Tier: Tier 1 — Image Classification
Tools: PyTorch, Google Colab, EfficientNet-B0, Grad-CAM

---

## PROJECT OVERVIEW
Proper waste sorting is critical for environmental sustainability. Manual sorting is slow, inconsistent, and often leads to contamination.

This project builds a deep learning system capable of classifying waste into six categories: cardboard, glass, metal, paper, plastic, trash.

The model uses EfficientNet-B0 transfer learning, balancing performance and computational efficiency.

---

## GOAL
Develop a computer vision model that accurately identifies waste types to support smart recycling workflows and reduce contamination.

---

## PROBLEM STATEMENT
Recycling facilities face major challenges:

- Misclassified waste contaminates recyclable materials
- Increased manual labor and processing time
- Lower recycling efficiency

Manual sorting is repetitive and inconsistent; an automated system improves accuracy and efficiency.

---

## PROPOSED SOLUTION
A transfer-learning-based CNN (EfficientNet-B0) is fine-tuned on a 6‑class waste dataset and evaluated with Grad-CAM.

Key Features:
- EfficientNet-B0 backbone
- Transfer learning
- PyTorch training pipeline
- Grad-CAM interpretability

---

## DATASET PLAN
Dataset: TrashNet-style
Total images: ~2527
Classes: cardboard, glass, metal, paper, plastic, trash

## Preprocessing:
- Resize, normalize
- Convert to tensors

## Augmentation:
- Random flips
- Rotations
- Color jitter

Fallback: Synthetic / Roboflow / Kaggle datasets if needed.

---

## SUCCESS METRICS
Accuracy ≥ 90%
Balanced per-class precision/recall
Grad-CAM must highlight correct areas

---

## PROJECT TIMELINE
Week 10 – Dataset + Setup
Week 11 – Training Baseline
Week 12 – Performance Improvements
Week 13 – Grad-CAM + Demo
Week 14 – Documentation & Polish
Week 15 – Presentation

---

## RISKS & MITIGATION
Low accuracy → Augmentation, LR tuning
Insufficient data → Roboflow, synthetic data
Overfitting → Early stopping, dropout
GPU limits → EfficientNet-B0, batch control

---

## REQUIRED RESOURCES
Compute: Google Colab GPU
Frameworks: PyTorch, Torchvision
Explainability: Grad-CAM
Cost: $0

---

REPOSITORY STRUCTURE
.
├── data/
│   └── README.md
├── models/
│   ├── trained/
│   └── README.md
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   └── README.md
├── results/
│   └── README.md
├── requirements.txt
├── docs/
│   └── MD_Tuozzo_Jose_ITAI1378.pdf
├── AI_usage_log.md
└── README.md

---

## HOW TO RUN THE PROJECT
1. Clone:
   git clone https://github.com/jtuozzo1616/Midterm---Final-Project-Proposal.git
   cd Midterm---Final-Project-Proposal
   pip install -r requirements.txt

2. Open:
   notebooks/01_data_exploration.ipynb  
   (Run in Google Colab w/ GPU)

3. Provide dataset manually or via Roboflow.

4. Run entire notebook:
   - Loads dataset  
   - Trains EfficientNet-B0  
   - Outputs evaluation metrics  
   - Produces Grad-CAM heatmaps  

---

## PERFORMANCE EVALUATION (SUMMARY)
Replace TODO with your real metrics.

Validation Accuracy: TODO
Test Accuracy: TODO
Common confusions: paper vs cardboard, plastic vs metal

Grad-CAM:
- Correct predictions focus on the waste item
- Wrong predictions focus on background or edges

Artifacts in:
results/loss_curve.png
results/confusion_matrix.png
results/gradcam_examples/

---

## FUTURE WORK
- Stronger backbones (EfficientNet-B2 / ResNet-50)
- Additional augmentation
- Deploy via ONNX / TorchScript
- Build Gradio / Streamlit UI
- Expand dataset diversity

---

## AI USAGE (SUMMARY)
AI was used for:
- Documentation structuring
- README formatting
- Concept clarification

All coding, dataset management, training, and debugging were done manually.

Full log:
AI_usage_log.md

---

## EXPECTED IMPACT
- Improves sorting accuracy
- Reduces contamination
- Supports sustainability initiatives
- Provides foundation for smart recycling bins or robotic sorters
