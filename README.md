# CNN_22-46829-1
### Assignment: CNN Development on Custom Dataset
**Course:** Computer Vision and Pattern Recognition (CVPR)  
**Student ID:** 22-46829-1  

---

## 📌 Project Overview
A custom Convolutional Neural Network (CNN) built from scratch using PyTorch 
to classify American Sign Language (ASL) hand gestures from the 
**Sign Language MNIST** dataset.

---

## 📁 Dataset
- **Name:** Sign Language MNIST
- **Source:** [Kaggle](https://www.kaggle.com/datasets/datamunge/sign-language-mnist)
- **Classes:** 24 (Letters A–Y, excluding J and Z which require motion)
- **Image Size:** 28×28 grayscale
- **Train Samples:** 27,455
- **Test Samples:** 7,172

---

## 🧠 Model Architecture
- 3 Convolutional Blocks (Conv → BatchNorm → ReLU → MaxPool)
- Filter progression: 1 → 32 → 64 → 128
- 2 Fully Connected Layers (1152 → 256 → 24)
- Dropout (p=0.5) for regularization
- Trained with and without Batch Normalization for comparison

---

## ⚙️ Training Details
| Hyperparameter | Value |
|---|---|
| Optimizer | Adam |
| Learning Rate | 0.001 |
| LR Scheduler | StepLR (step=10, γ=0.5) |
| Loss Function | CrossEntropyLoss |
| Epochs | 30 |
| Batch Size | 64 |

---

## 📊 Results
- Comprehensive metrics: Precision, Recall, F1-Score per class
- Training/Validation Loss & Accuracy curves
- Confusion Matrix (24×24)
- Per-class accuracy breakdown

---

## 📂 Repository Structure
```
CNN_22-46829-1/
│
├── CNN_22-46829-1.ipynb   # Full implementation notebook
├── CNN_22-46829-1.pth     # Saved model weights
└── README.md              # Project documentation
```

---

## 🚀 How to Run
1. Open `CNN_22-46829-1.ipynb` in Google Colab
2. Enable GPU: `Runtime → Change runtime type → T4 GPU`
3. Upload `sign_mnist_train.csv` and `sign_mnist_test.csv` from Kaggle
4. Run all cells top to bottom

---

## 🛠️ Libraries Used
- PyTorch & Torchvision
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
