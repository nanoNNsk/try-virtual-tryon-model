# 👕 Ultimate ComfyUI VTON Studio (Final Production Build)
> **Fully Patched & Multi-Model Integration for Google Colab**

[![Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-orange?logo=googlecolab)](https://colab.research.google.com/)
[![ComfyUI](https://img.shields.io/badge/Engine-ComfyUI%20v1.0-blueviolet)](https://github.com/comfyanonymous/ComfyUI)
[![SOTA](https://img.shields.io/badge/Models-2025%20Verified-green)](#)

---

## 🌟 Overview
โปรเจกต์นี้คือ Unified VTON Sandbox ที่รวมการตั้งค่าที่ดีที่สุดสำหรับการทำ Virtual Try-On บน Cloud GPU โดยเน้นความเสถียรผ่านระบบ **"Global Vaccine"** เพื่อแก้ปัญหา Dependency Conflict ในสภาพแวดล้อมของ Google Colab โดยเฉพาะ

---

## 🧠 Supported Models & Repositories
(ตรวจสอบแล้วตรงตาม Source Code 100%)

| Model | Repository Source | Key Dependencies |
| :--- | :--- | :--- |
| **IDM-VTON** | `TemryL/ComfyUI-IDM-VTON` | ControlNet-Aux, Segment-Anything |
| **CatVTON** | `chflame163/ComfyUI_CatVTON_Wrapper` | Diffusers 0.25.0, Transformers 4.38.2 |
| **OOTDiffusion** | `AuroBit/ComfyUI-OOTDiffusion` | Human Parsing Binaries |
| **FitDiT** | `BoyuanJiang/FitDiT-ComfyUI` | DiT Architecture Support |

---

## 🛠️ System Architecture & Fixes
เราไม่ได้แค่ติดตั้ง แต่เรา **"Patch"** ระบบเพื่อให้รันได้จริง:

* **🛡️ VRAM Optimization:** เปิดใช้ `expandable_segments` เพื่อลดปัญหา Memory Fragmentation
* **☢️ Global Vaccine:** บังคับใช้ `numpy<2` และ `onnxruntime` เพื่อป้องกันระบบล่มจาก Library รุ่นใหม่ที่เข้ากันไม่ได้
* **🔨 The Hammer Fix:** ระบบติดตั้ง Dependencies แบบแยกโมเดล (Force Stable Versions) เช่น:
    * **IDM-VTON:** ล็อก `diffusers==0.27.2` และ `transformers==4.40.2`
    * **Others:** ล็อก `diffusers==0.25.0` เพื่อความเข้ากันได้ของสถาปัตยกรรมเก่า

---

## 🚀 How to Use
1.  **Select Target:** เลือก Model ที่ต้องการผ่านหน้า UI ของ Colab (`TARGET_NODE`)
2.  **Environment Setup:** ระบบจะทำการ Clone Repo และติดตั้ง Requirement ตามที่คุณเลือกโดยอัตโนมัติ
3.  **Fast Download:** ใช้ `aria2c` ดึง Weights จาก Hugging Face ด้วยความเร็วสูง
4.  **Secure Launch:** เข้าใช้งานผ่าน **Cloudflare Tunnel** (ไม่ต้องใช้ Token)

---

## 🤝 Credits & Acknowledgments
ขอบคุณเจ้าของ Repository ที่เรานำมาใช้ใน Code ชุดนี้:
* **IDM-VTON Logic:** [TemryL](https://github.com/TemryL/ComfyUI-IDM-VTON)
* **Auxiliary Tools:** [Fannovel16 (ControlNet)](https://github.com/Fannovel16/comfyui_controlnet_aux), [storyicon (SAM)](https://github.com/storyicon/comfyui_segment_anything)
* **CatVTON Wrapper:** [chflame163](https://github.com/chflame163/ComfyUI_CatVTON_Wrapper)
* **OOTDiffusion Port:** [AuroBit](https://github.com/AuroBit/ComfyUI-OOTDiffusion)
* **FitDiT Integration:** [BoyuanJiang](https://github.com/BoyuanJiang/FitDiT-ComfyUI)
* **Base Engine:** [ComfyUI](https://github.com/comfyanonymous/ComfyUI) & [ComfyUI-Manager](https://github.com/ltdrdata/ComfyUI-Manager)

---
*Developed & Patched by **nano***