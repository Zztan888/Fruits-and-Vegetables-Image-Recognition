# 🍎 Fruits and Vegetables Image Recognition

This repository contains a Deep Learning project for the automated classification of fruits and vegetables. Using a **Convolutional Neural Network (CNN)**, the model identifies various categories of produce from image data, facilitating applications in automated retail and food processing.

---

## 📑 Project Components
* **Dataset:** [Fruits and Vegetables Image Recognition](https://www.kaggle.com/datasets/kritikseth/fruit-and-vegetable-image-recognition/data) (Kaggle)
* **Goal:** Multi-class Image Classification
* **Language/Framework:** Python, TensorFlow/Keras
* **Reporting Format:** IEEE Standard

---

## 📂 Quick Links
* 📓 **Jupyter Notebook:** [Fruit and Vegetable_Project 2.ipynb](./Fruit%20and%20Vegetable_Project%202.ipynb)
* 📄 **Technical Report (IEEE):** [Project2_report_IEEE.pdf](./Project2_report_IEEE.pdf)
* 📊 **Dataset Source:** [Kaggle Dataset Link](https://www.kaggle.com/datasets/kritikseth/fruit-and-vegetable-image-recognition/data)

---

## 🏗️ Model Architecture
The project implements a deep CNN architecture designed to extract spatial hierarchies from RGB images.



### Architecture Summary:
1. **Input Layer:** Resized images (e.g., $224 \times 224 \times 3$).
2. **Convolutional Layers:** Multiple layers with $3 \times 3$ kernels to detect features like textures and colors of different produce.
3. **Activation Function:** **ReLU** (Rectified Linear Unit) used across hidden layers to handle non-linearity:
   $$f(x) = \max(0, x)$$
4. **Pooling Layers:** Max-Pooling layers to reduce spatial dimensions and prevent overfitting.
5. **Dropout Layer:** To improve generalization by randomly deactivating neurons during training.
6. **Output Layer:** Fully connected (Dense) layer with a **Softmax** activation function to output probabilities for each class:
   $$\text{Softmax}(z_i) = \frac{e^{z_i}}{\sum_{j} e^{z_j}}$$

---

## 💻 Implementation Workflow
The solution in `Fruit and Vegetable_Project 2.ipynb` includes:
* **Data Augmentation:** Using `ImageDataGenerator` to flip, rotate, and zoom images, increasing the model's ability to recognize produce in different orientations.
* **Pre-processing:** Normalizing pixel values to the range $[0, 1]$.
* **Training:** Utilizing the **Adam** optimizer and **Categorical Cross-Entropy** loss.

---

## 📊 Results Analysis
The model's performance is evaluated based on:
* **Classification Accuracy:** Overall success rate across all fruit/vegetable categories.
* **Confusion Matrix:** Identifying specific classes that the model might confuse (e.g., similar-looking green vegetables).
* **Training Curves:** Analysis of loss and accuracy over epochs to ensure no overfitting occurred.



---

## 🚀 How to Run
1. Download the dataset from Kaggle and place it in a folder named `train`, `test`, and `validation`.
2. Install dependencies:
   ```bash
   pip install tensorflow matplotlib numpy
