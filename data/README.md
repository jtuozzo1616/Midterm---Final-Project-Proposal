# Dataset Information

This project uses a TrashNet-style waste classification dataset containing 6 classes:

- Cardboard  
- Glass  
- Metal  
- Paper  
- Plastic  
- Trash  

### 📊 Dataset Size
~2527 images total  
Split into: train / validation / test sets  

### 🧼 Preprocessing
- Resize to 224x224
- Normalization (ImageNet mean/std)
- Data augmentation: random flip, rotation

### 🌍 Source
Public waste classification dataset (similar to TrashNet)  
Used strictly for academic purposes.

If dataset unavailable → fallback to synthetic / Roboflow dataset for reproducibility.
# Data

- Dataset type: TrashNet-style waste classification
- Classes: cardboard, glass, metal, paper, plastic, trash
- Size: ~2,500+ images (train/val/test)
- Source: Public dataset (Roboflow / Kaggle / GitHub)
- Structure:
data/
train/class_name/
val/class_name/
test/class_name/
