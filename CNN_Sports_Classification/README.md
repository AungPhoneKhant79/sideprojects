# 🏅 Sports Classification (100 Classes)

I trained a CNN to classify images of **100 different sports** (~50k images).  
Using **EfficientNetB0 with transfer learning**, the model reached **97.6% test accuracy** (close to the reference benchmark of 98%).

---

## How it works
- Dataset: clean Kaggle set (224×224 images, pre-split train/val/test).  
- Preprocessing: data augmentation (flips, zooms, rotations).  
- Model: EfficientNetB0 backbone (ImageNet pretrained) → global pooling → dense softmax head.  
- Training: first froze the backbone, then fine-tuned upper layers with a lower LR.  

---

## Results
- **Test accuracy:** 97.6%  
- **Artifacts:**  
  - [Confusion Matrix (normalized)](analysis_outputs/confusion_matrix_normalized.png)  
  - [Classification Report](analysis_outputs/classification_report.csv)

---

## Mistakes worth noting
The model sometimes confuses visually similar sports:  
- BMX ↔ Motorcycle Racing  
- Frisbee ↔ Shotput  
- Ice Climbing ↔ Rock Climbing  
- Snowboarding ↔ Giant Slalom  
- Ultimate Frisbee ↔ Rugby  

These errors highlight the challenge of **fine-grained classification** at 224×224 resolution.

---

## What I learned
- How transfer learning speeds up training and improves accuracy.  
- Why freezing/unfreezing backbones matters.  
- Saved models keep both the architecture + learned weights → instant reload for evaluation.  
- Looking at **failure cases** (not just accuracy) is crucial.

---

## Tech
TensorFlow/Keras, EfficientNetB0, NumPy, Pandas, Matplotlib, scikit-learn
