# FII-NX3Intl-Aarav-Kumar

# AI Crop Disease Detection - NexHax Submission

This repository contains the code for my submission to the **FII-NX3 NexHax Hackathon**. The project is a deep learning model designed to identify 38 different plant diseases from leaf images.

## 🎯 Problem Statement & SDG Alignment

This tool directly addresses the **UN's Sustainable Development Goal #2 (Zero Hunger)**, specifically focusing on **Target 2.4**: *ensure sustainable food production systems*.

Globally, up to 40% of food crops are lost annually due to plant pests and diseases. By providing farmers with a fast, accessible, and accurate method for early disease detection, this tool can help reduce crop losses, minimize pesticide use, and promote greater food security.

## 🛠️ How It Works

The core of the project is a computer vision model built using the PyTorch framework. The implementation follows modern deep learning best practices:

* **Model:** A `ResNet18` architecture.
* **Technique:** **Transfer Learning & Fine-Tuning**. The model was pre-trained on the ImageNet dataset and then fine-tuned on the specific task of plant disease classification. The final two convolutional blocks were unfrozen to adapt the model's feature extraction capabilities.
* **Dataset:** The model was trained on the **"New Plant Diseases Dataset"** from Kaggle, which contains over 87,000 images across 38 distinct classes.
* **Training:** The model was trained for 20 epochs using the Adam optimizer and a learning rate scheduler (`StepLR`) to improve performance.

## 📊 Key Results

After the full training and fine-tuning process, the model achieved a final validation accuracy of:

## **99.63%**

## 🚀 How to Run the Code

The entire project is contained within the `.ipynb` notebook file.

1.  **Open the `.ipynb` file in Google Colab.**
2.  Ensure the runtime is set to use a **`T4 GPU`** for hardware acceleration (`Runtime -> Change runtime type`).
3.  Run the cell in **Section 2** and upload your personal `kaggle.json` API key when prompted.
4.  Run all subsequent cells sequentially from top to bottom. The notebook will handle data download, preprocessing, model training, and prediction.
5.  The final section of the notebook demonstrates the model's `predict_image` function on sample images.
