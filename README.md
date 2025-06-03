# Siamese Network with Contrastive Loss on MNIST + Generating Embeddings for images🧠
This project implements a Siamese Neural Network using Keras to learn a similarity metric on the MNIST dataset. The network is trained with **contrastive loss** to distinguish between similar and dissimilar image pairs, enabling it to recognize digits based on learned embeddings.

## What is Siamese Network?
A Siamese Network is a type of neural network architecture specifically designed to learn similarity between pairs of inputs.

![image](https://github.com/user-attachments/assets/49784c63-625e-4820-a87f-fffc15bd9e4e)

## What is Contrastive Learning?
Contrastive Learning is a self-supervised or supervised learning technique where a model learns by comparing data points-specifically by pulling similar items closer in the embedding space and pushing dissimilar items farther apart.

## 📌 Overview
- Builds a Siamese network using twin convolutional neural networks (CNNs).
- Trained on image pairs (same and different digits).
- Uses **contrastive loss** to bring similar images closer in embedding space while pushing dissimilar ones apart.
- Visualizes embeddings and compares Euclidean distances to verify learning.

## 🧪 Dataset
- MNIST: Handwritten digit dataset.
- Contains 60,000 training and 10,000 test grayscale images of size 28x28 pixels.

## 🚀 How It Works
### 1. Data Preparation
- Normalizes and reshapes images.
- Creates positive (same digit) and negative (different digits) image pairs.
- Assigns labels: `0` for similar, `1` for dissimilar.

### 2. Model Architecture
- A **base CNN** (shared weights) is used to extract embeddings.
- A Lambda layer computes the Euclidean distance between image embeddings.
- Final model is trained using **contrastive loss**.

### 3. Evaluation
- After training, embeddings for different digits are compared.
- Small distance => Same digit (similar)
- Large distance => Different digit (dissimilar)

## Install dependencies using:
pip install tensorflow numpy matplotlib

## ▶️ Usage
Run the script: contrastive-learning-embedding.ipynb

