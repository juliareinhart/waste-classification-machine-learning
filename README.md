# 🌸 RealWaste Classification: Machine Learning for Waste Sorting

## Overview

This project uses the RealWaste image dataset to train and compare deep learning models for waste classification. The goal is to classify waste images into categories such as cardboard, glass, metal, paper, plastic, food organics, textile trash, vegetation, and miscellaneous trash.

This was completed as a group project for Applied Machine Learning.

## 🎥 Demo Video

YouTube Demo:

[![Watch the demo](https://img.youtube.com/vi/y1gl1z02Ww0/0.jpg)](https://youtu.be/y1gl1z02Ww0)

## 👥 Team Project

This project was developed collaboratively.

Team Members:

- Julia Reinhart — [@juliareinhart](https://github.com/juliareinhart)
- Amiel Nava — [@AmielCyber](https://github.com/AmielCyber)
- Carlos Cazares — [@cgcazares1](https://github.com/cgcazares1)

## Dataset

Dataset: [RealWaste - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/908/realwaste)

Original research paper:  
[RealWaste: A Novel Real-Life Data Set for Landfill Waste Classification Using Deep Learning](https://www.mdpi.com/2078-2489/14/12/633)

The RealWaste dataset is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/legalcode).

## Classes

The dataset contains 4,752 images across 9 waste categories:

| Class               | Image Count |
| ------------------- | ----------: |
| Cardboard           |         461 |
| Food Organics       |         411 |
| Glass               |         420 |
| Metal               |         790 |
| Miscellaneous Trash |         495 |
| Paper               |         500 |
| Plastic             |         921 |
| Textile Trash       |         318 |
| Vegetation          |         436 |

## Project Objective

The objective is to classify waste images using multiple CNN-based deep learning architectures and compare their performance.

Models explored include:

- MobileNet
- EfficientNetB0
- GoogleNet
- YOLOv8 Classification
- YOLOv8 Detection

## Machine Learning Approach

This is a supervised learning image classification project. Each image is labeled with a waste category, and models are trained to predict the correct class.

The project includes:

- Data preprocessing
- Train/validation/test splitting
- Data augmentation
- CNN model training
- Transfer learning
- Hyperparameter tuning
- Confusion matrix analysis
- Model performance comparison

## Assumption

Waste that does not clearly belong to cardboard, food organics, glass, metal, paper, plastic, textile trash, or vegetation is classified as miscellaneous trash.

## Repository Structure

```text
waste-classification-machine-learning/
│
├── README.md
│
├── Model 1 CNN/
│   ├── models/
│   │   ├── best_googlenet_realwaste.pth
│   │   ├── efficientnet_b0_realwaste.pth
│   │   └── mobilenetv3_realwaste.pth
│   │
│   ├── requirements.txt
│   └── waste_classification.ipynb
│
├── Model 2 YOLO Classification/
│   ├── PyTorch_YOLOv8n_hp_baseline.ipynb
│   ├── PyTorch_YOLOv8n_hp_with_stratified_split.ipynb
│   ├── PyTorch_YOLOv8n_hp_with_stratified_split_combined_with_data_augmentation.ipynb
│   └── PyTorch_YOLOv8n_hp_with_stratified_split_freeze.ipynb
│
├── Model 3 YOLO Detection/
│   └── PyTorch_YOLOv8n_hp_data.ipynb
│
├── WasteClassificationReport.pdf
│
└── .gitignore
```

## How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/juliareinhart/waste-classification-machine-learning.git
cd waste-classification-machine-learning
```

### 2. Create a Python Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If a `requirements.txt` file is not available yet, install the main libraries manually:

```bash
pip install torch torchvision matplotlib pandas numpy scikit-learn ultralytics jupyter
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

Then open the notebook for the model you want to run.

---

## Results

Results include accuracy scores, training curves, confusion matrices, and normalized confusion matrices for model comparison.

Add final results here:

| Model Name        | Task Type                            | GFLOPS | Training Time | Top 5 Accuracy | Top 1 Accuracy |
| ----------------- | ------------------------------------ | -----: | ------------- | -------------: | -------------: |
| YOLOv8n-cls       | Classification                       |   12.5 | < 1 hour      |         99.72% |         90.18% |
| YOLOv8n Detection | Object Detection (Box Labels Needed) |   28.8 | ~ 3 hours     |            N/A |          89.2% |
| GoogleNet         | Classification                       |    1.5 | < 1 hour      |         97.79% |         87.39% |
| MobileNetV3       | Classification                       |   0.06 | < 1 hour      |         99.37% |         86.13% |
| EfficientNetB0    | Classification                       |   0.39 | < 1 hour      |         99.58% |         77.52% |

---

## Technologies Used

- Python
- PyTorch
- Torchvision
- Ultralytics YOLOv8
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Git/GitHub

---

## License

This project uses the MIT License for the code in this repository.

The dataset is licensed separately under the Creative Commons Attribution 4.0 International License.

---

## Acknowledgments

Special thanks to the creators of the RealWaste dataset and the UCI Machine Learning Repository for making the dataset available for research and educational use.
