# DogVsCat
# 🐶🐱 Cats vs Dogs Classification using HOG + SVM

This project demonstrates image classification of cats and dogs using **Histogram of Oriented Gradients (HOG)** features combined with a **Linear Support Vector Machine (SVM)** classifier. It serves as a practical example of classical computer vision techniques for image recognition without deep learning.

---

## 📖 Project Overview

The goal is to classify images from the **Microsoft Cats vs Dogs dataset** into two categories: **cats** and **dogs**. Unlike deep learning approaches, this project uses **feature extraction** with HOG descriptors and a classical machine learning algorithm (SVM) to perform classification.

Key steps include:

1. **Dataset Loading**
   - A subset of the dataset is loaded for faster execution.
   - Images are resized to a uniform size (`IMG_SIZE = 128`) for consistency.
   - Corrupted or unreadable images are skipped automatically.

2. **Feature Extraction**
   - Images are converted to grayscale.
   - HOG (Histogram of Oriented Gradients) features are extracted for each image.
   - HOG captures the shape and texture information of objects in the image.

3. **Model Training**
   - Features are scaled using `StandardScaler` to improve SVM performance.
   - A **Linear SVM** classifier is trained on the extracted features.
   - The dataset is split into training and validation sets for evaluation.

4. **Evaluation**
   - Validation accuracy is reported.
   - Classification report shows precision, recall, and F1-score.
   - Confusion matrix visualizes correct and incorrect predictions.
   - Sample images are displayed with predicted and true labels.

---


## 🛠️ How to Run

### Option 1: Google Colab
1. Open `Cats_vs_Dogs_HOG_SVM.ipynb` in [Google Colab](https://colab.research.google.com/).  
2. Install required packages if not already installed:
   ```bash
   !pip install numpy opencv-python scikit-learn scikit-image matplotlib tqdm kagglehub
3. Run all notebook cells sequentially. The dataset will be downloaded using kagglehub.
