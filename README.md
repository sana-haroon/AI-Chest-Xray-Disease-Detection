# AI-Chest-Xray-Disease-Detection
Multi-label chest X-ray disease classification using DenseNet121 transfer learning and Grad-CAM.
A Deep Learning project using **DenseNet121 Transfer Learning** to identify multiple chest X-ray findings from a single image.

## Project Overview

This project develops a multi-label chest X-ray classification model using the NIH ChestX-ray14 dataset. It predicts the presence or absence of six selected labels.

## Dataset

- **Dataset:** NIH ChestX-ray14
- **Input Image Size:** 224 × 224
- **Image Format:** RGB
- **Number of Classes:** 6

Selected labels:
1. Atelectasis
2. Cardiomegaly
3. Effusion
4. Edema
5. Consolidation
6. No Finding

Dataset source: [NIH ChestX-ray14 on Kaggle](https://www.kaggle.com/datasets/nih-chest-xrays/data)

## Model Architecture

- Pretrained DenseNet121
- Transfer Learning
- Sigmoid activation for multi-label predictions
- BCEWithLogitsLoss
- ImageNet normalization
- Data augmentation

## Explainability

Grad-CAM is used to visualize image regions that contribute to model predictions.

## Model Weights

Download the trained model from the GitHub Release:

[Download DenseNet121 Model Weights](../../releases/tag/v1.0)

The release includes `final_densenet121.pth`.

## Project Files

- `multi-label-chest-x-ray-classification-using-transferLearning.ipynb` — Complete project notebook
- `model_config.json` — Model configuration
- `final_test_results.csv` — Test evaluation results
- `final_thresholds.csv` — Optimized classification thresholds
- GitHub Release — Trained model weights

## Evaluation Results

| Metric | Score |
|---|---:|
| Macro F1-score | 0.3340 |
| Micro F1-score | 0.4209 |
| Exact Match Accuracy | 0.2632 |
| Hamming Accuracy | 0.7690 |

Performance varies across individual disease labels. Please refer to `final_test_results.csv` for detailed results.

## Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Grad-CAM

## Limitations

This project is an educational research prototype and is **not intended for clinical diagnosis**. Predictions may contain false positives and false negatives. The dataset labels are derived from radiology reports and may contain uncertainty.

---

If you find this project useful, feel free to explore the repository.
