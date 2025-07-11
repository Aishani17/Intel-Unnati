
# 🔍 Image Sharpening using Knowledge Distillation

## 📌 Overview

This project focuses on enhancing **image sharpness** using an efficient **knowledge distillation** approach, combining the power of deep neural networks with the practicality of deploying lightweight student models. Leveraging large-scale facial image datasets, our work demonstrates how a **teacher-student architecture** can achieve high Structural Similarity Index (SSIM) while being optimized for real-time applications.

## 🎯 Problem Statement

> **"Image Sharpening using Knowledge Distillation"**

Modern applications demand high-quality, sharp images even in low-resource scenarios (e.g., embedded devices, mobile apps). This project aims to distill the sharpening capability of a complex teacher network into a lightweight student model, enabling **real-time deployment** without compromising visual quality.

## 👨‍💻 Project Contributors

- **Eesha Thottempudi**
- **Aishani Tetali**
- **Aithi Mouleendra**
- **Mentored by:** *Sheik Khadar Ahmad Manoj*

## 🧠 Methodology

### 🧪 1. Dataset

We utilized the following datasets for training and evaluation:

- 📁 [CelebA Dataset](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset): A large-scale face dataset with more than 200,000 celebrity images, covering variations in facial attributes.
- 📁 [Image Quality Dataset](https://www.kaggle.com/datasets/kamalsinghparmar/dataset): Supplemented to validate sharpening performance on generic blurred images.

### 🧠 2. Model Architecture

#### 🏫 Teacher Model
- Deep convolutional neural network trained on blurred-sharp image pairs.
- Outputs high-clarity reference images used for training the student model.

#### 👨‍🎓 Student Model
- Lightweight CNN designed to mimic the teacher model’s outputs.
- Trained using **SSIM-based loss** and **L1 distance**, optimized with:
  - Distillation Loss: Combines perceptual and pixel losses.
  - Real-time constraints: Reduced parameters without sacrificing accuracy.

### 🔄 Training Pipeline

1. Blur simulation applied to high-quality images.
2. Teacher network generates sharpened targets.
3. Student model learns to replicate teacher outputs.
4. Evaluation based on SSIM and MSE metrics.

## 📂 Repository Structure

```
📦 Image-Sharpening-KD
├── teacherintel.ipynb            # Teacher model training and evaluation
├── A1StudentModel.ipynb          # Distilled student model implementation
├── Teacher_Student_Kd_ngrok_.ipynb # Integrated workflow with ngrok (for real-time deployment)
├── README.md                     # Project description and documentation
```

## 📊 Results

| Model        | SSIM Score | MSE Loss | Parameters |
|--------------|------------|----------|------------|
| Teacher      | **0.93+**  | ~0.01    | High       |
| Student      | **0.91+**  | ~0.02    | Low (efficient for deployment) |

> ✅ **Student model nearly matches teacher performance while being lightweight and deployable.**

## 🚀 Deployment

- We enabled real-time image sharpening using **ngrok** and a Flask API (as included in the ngrok-based notebook).
- The student model can be embedded into low-power edge devices and deployed via REST APIs for online image enhancement.

## 🧪 Future Improvements

- Integrate **attention-based distillation** techniques.
- Explore **GAN-based refinement** for better texture restoration.
- Deploy using **TensorFlow Lite** or **ONNX** for edge optimization.

## 🤝 Acknowledgments

We extend our sincere gratitude to our mentor **Sheik Khadar Ahmad Manoj** for his constant support and guidance throughout the project. This project was submitted under the **Intel Unnati** initiative.

## 📫 Contact

For queries or collaborations, reach out to:
- **Eesha Thottempudi**
- **Aishani Tetali**
- **Aithi Mouleendra**
