# Skin Cancer U-Net Preprocessing

This repository provides the **preprocessing pipeline** used in a skin cancer detection project. The focus is on **segmenting dermoscopic images** of skin lesions using a U-Net-based model to improve lesion visibility and remove background noise before classification.

## 🧪 Overview

To enhance the performance of our classification model, we applied a preprocessing step that includes:
- **Image resizing** to 64x64 pixels
- **Grayscale conversion** to simplify input without losing lesion features
- **Lesion segmentation** using a custom-built **U-Net model**

This helps isolate skin lesions more effectively, allowing downstream classifiers to focus on relevant areas.

## 🧠 U-Net Model

The U-Net model follows an **encoder-bottleneck-decoder** structure:
- The **encoder** captures spatial features through convolution and pooling.
- The **bottleneck** processes compressed feature representations.
- The **decoder** upsamples and combines these features with earlier layers (via skip connections) to preserve details and output a precise **segmentation mask**.

The final mask highlights lesion regions, enabling clean cropping or focused analysis.

## 📁 Preprocessed Dataset

The preprocessed dataset (segmented and standardized images) is publicly available on Kaggle:

🔗 [Skin Cancer Preprocessed Dataset](https://www.kaggle.com/datasets/rutvik23/skin-cancer-preprocessed)

This dataset is ready to be used for skin cancer classification tasks or further medical image analysis.

## 💡 Applications

- **Skin lesion classification**
- **Image-based medical diagnostics**
- **Lesion detection model training**
- **Auto-cropping or ROI enhancement**

## ⚙️ Tech Stack

- TensorFlow / Keras
- OpenCV
- NumPy, Matplotlib
- Kaggle Notebook

