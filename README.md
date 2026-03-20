# 👕 Virtual Try-On Master Playground (Experimental)

A unified, research-oriented playground designed to compare and test state-of-the-art (SOTA) AI models for Virtual Try-On (VTON). This project provides a streamlined experience via **ComfyUI** on **Google Colab**, allowing you to switch between different high-performance models in a single interface.

## 🌟 Project Overview
This project serves as an all-in-one testing sandbox for garment transfer. By utilizing cloud-based GPUs, it overcomes hardware limitations of local machines (like the Lenovo IdeaPad Slim 3) to provide fast, high-quality results.

## 🚀 Supported Models
Access all these models through the **Unified Selection Menu** in the Master Notebook:
*   **IDM-VTON:** Superior garment detail preservation.
*   **CatVTON:** Lightweight, efficient, and versatile.
*   **OOTDiffusion:** Realistic garment warping and natural blending.
*   **FitDiT:** Cutting-edge Diffusion Transformer (DiT) architecture for complex folds.
*   **Any2Any:** High-fidelity image-to-image transformation (2025 SOTA).
*   **Outfit Anyone:** High-quality results across various body shapes (by HumanAIGC/Alibaba).

## ✨ Key Features
*   **Unified Notebook (`VTON_Master_Playground.ipynb`):** No more switching between multiple files. Select your model via a simple dropdown menu.
*   **Optimized Performance:** Uses `aria2c` for ultra-fast model downloads from Hugging Face.
*   **Instant Access:** Integrated Cloudflare Tunnel for quick access to the ComfyUI web interface.
*   **User-Friendly:** Interactive forms allow you to configure settings without touching the code.

## 🛠️ Getting Started (Google Colab)

1.  **Open the Notebook:** Upload `VTON_Master_Playground.ipynb` to [Google Colab](https://colab.research.google.com/).
2.  **Set Hardware Accelerator:** Go to `Runtime` > `Change runtime type` and select **T4 GPU**.
3.  **Run Step 1 (Setup):** Installs ComfyUI and the essential manager.
4.  **Run Step 2 (Model Install):** Select your desired model (e.g., IDM-VTON) from the dropdown and run the cell.
5.  **Run Step 3 (Launch):** Wait for the **`trycloudflare.com`** link to appear and click it to open the UI.

## 🤝 Credits & Acknowledgments
*   **ComfyUI-On-Colab:** Inspiration and foundation from [nazdridoy/ComfyUI-On-Colab](https://github.com/nazdridoy/ComfyUI-On-Colab).
*   **ComfyUI:** The core interface by [comfyanonymous](https://github.com/comfyanonymous/ComfyUI).
*   **Model Researchers:** Special thanks to the teams behind IDM-VTON, CatVTON, OOTDiffusion, FitDiT, Any2Any, and Outfit Anyone.

---
*Developed by **nano***
