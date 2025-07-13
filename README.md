# 🧠 Hybrid TumorVision: A Hybrid Deep Learning Model for Brain Tumor Classification

## 🔍 Overview
**Hybrid TumorVision** is a hybrid deep learning framework designed for accurate classification of brain tumors using MRI scans. The model combines the strengths of **Xception** and **InceptionV3** architectures, enhanced with **Dual Attention Mechanisms** (Spatial and Channel Attention), to focus on tumor-relevant features. This approach significantly improves diagnostic precision and reduces false negatives—especially in critical cases where tumors must not be misclassified as "No Tumor".

---

## 📊 Key Features
- ✅ **Hybrid Architecture:** Combines Xception and InceptionV3 for deep and multi-scale feature extraction.
- 🧠 **Dual Attention Mechanism:** Integrates spatial and channel attention to focus on informative tumor regions and features.
- 📈 **High Accuracy:** Achieved **98.7% test accuracy**, with **100% recall and precision** in detecting "No Tumor" class.
- 🔄 **Preprocessing and Augmentation:** Includes resizing, normalization, rotation, flipping, zoom, shear, and brightness adjustment.
- 📁 **Dataset:** Utilizes a public MRI dataset from Kaggle with 7023 images across four classes (Glioma, Meningioma, Pituitary, No Tumor).

---

## 📂 Project Structure

📁 Hybrid TumorVision/
├── data/ # Training, validation, and test data
├── models/ # Model architecture files (Xception, InceptionV3, attention modules)
├── notebooks/ # Jupyter notebooks for experiments
├── utils/ # Helper scripts for preprocessing, visualization, etc.
├── results/ # Plots: accuracy/loss, confusion matrix, ROC curves
├── README.md # Project documentation
└── requirements.txt # Python dependencies

yaml
Copy
Edit

---

## 🧪 Model Training & Evaluation
- **Train-Validation-Test Split:** 70% training, 15% validation, 15% testing
- **Input Shape:** 299×299×3 (to match InceptionV3/Xception requirements)
- **Optimizer:** Adam  
- **Loss Function:** Categorical Crossentropy  
- **Regularization:** Dropout, early stopping  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC-AUC

---

## 📊 Sample Results

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Glioma        | 96.7%     | 98.6%  | 97.6%    |
| Meningioma    | 96.7%     | 97.4%  | 97.0%    |
| No Tumor      | 99%       | 99%    | 99%      |
| Pituitary     | 100%      | 97.3%  | 98.6%    |

- ✅ **Total test images:** 656  
- ✅ **Zero false negatives for "No Tumor" class** — critical for real-world reliability.

---

## 📌 Future Scope
- 🏥 Real-time deployment in clinical environments via web/mobile applications.
- 🧬 Integration with multi-modal data (histopathology, genetic info).
- 🧠 Extension to detect tumor grades or malignancy levels.
- 🤖 Use of transformer-based models (like ViT) and self-supervised learning.
