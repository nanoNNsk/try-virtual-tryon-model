# 👕 Virtual Try-On Playground (Experimental)

A research-oriented playground to compare state-of-the-art (SOTA) AI models for Virtual Try-On (VTON). This project provides a unified UI to test and evaluate various diffusion-based clothing transfer models.

## 🌟 Project Overview
This project serves as a testing sandbox to compare the performance of different AI models in transferring garments onto a person. Users can upload a source person image and a target garment image, then select from a variety of models to see how each handles realism, texture preservation, and body alignment.

## 🚀 Supported Models
The playground integrates several high-performance models:
*   **IDM-VTON:** High-fidelity garment detail preservation using Improved Diffusion Models.
*   **OOTDiffusion:** Out-of-the-box garment warping and blending using latent diffusion.
*   **CatVTON:** A flexible and lightweight approach to virtual try-on.
*   **FitDiT:** Utilizing Diffusion Transformers (DiT) for complex clothing structural integrity.
*   **Outfit Anyone:** Alibaba's versatile model capable of handling various body shapes and styles.

## ✨ Key Features
*   **Multi-Model Selection:** Seamlessly switch between different VTON models through the UI.
*   **Intuitive Workflow:** Simple upload system for Person and Garment images.
*   **Interactive UI:** A clean interface designed for quick experimentation and comparison.
*   **Real-time Processing:** Run models and view output directly within the application.

## 🛠️ Getting Started

### 1. Environment Setup
```bash
# Clone the repository
git clone https://github.com/nano/try-virtual-tryon-model.git
cd try-virtual-tryon-model

# Create a Virtual Environment
python -m venv venv
# Activate on Windows:
venv\Scripts\activate
# Activate on Linux/macOS:
source venv/bin/activate

# Install Dependencies
pip install -r requirements.txt
```

### 2. Running the Application
```bash
python app.py
```

## 📖 How to Test
1.  **Select Model:** Choose your preferred model (e.g., IDM-VTON or Outfit Anyone) from the dropdown menu.
2.  **Upload Images:**
    *   **Person Image:** Upload the photo of the person you want to dress.
    *   **Garment Image:** Upload the photo of the piece of clothing.
3.  **Generate:** Click the **"Run"** or **"Generate"** button.
4.  **View Results:** Wait for the AI to process and display the final transformed image in the Output section.

## 📌 Disclaimer
This project is for experimental and educational purposes only. Performance may vary depending on GPU resources and the quality of the input images.

---
*Developed by **nano***
