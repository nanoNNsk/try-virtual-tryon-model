# 👕 Ultimate ComfyUI VTON Studio (Final Production Build)
> **The Most Stable & Performance-Optimized VTON Sandbox for Google Colab**

[![Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-orange?logo=googlecolab)](https://colab.research.google.com/)
[![License](https://img.shields.io/badge/License-Experimental-yellow)](#)
[![Version](https://img.shields.io/badge/Version-2026.Final.Patched-blue)](#)

---

## 🌟 Overview
**Ultimate ComfyUI VTON Studio** คือโปรเจกต์ระดับ "Final Production Build" ที่ถูกออกแบบมาเพื่อนักวิจัยและ AI Engineer โดยเฉพาะ รวบรวม SOTA (State-of-the-Art) Virtual Try-On Models ไว้ในโครงสร้างที่ถูก **"Hardened"** (เสริมความแข็งแกร่ง) เพื่อรันบน Google Colab ได้โดยไม่แครช

### 🛡️ Why "Patched"?
ในฐานะ AI Engineer เรามักพบปัญหา "Library Conflict" (เช่น Numpy 2.0 ทำงานไม่ได้กับโมเดลเก่า) สคริปต์ตัวนี้จึงประกอบด้วย:
* **Global Vaccine:** บังคับติดตั้ง Library เฉพาะเจาะจงเพื่อกันระบบพัง (Numpy < 2.0, ONNX Runtime Patch)
* **VRAM Fragmentation Fix:** ใช้ `expandable_segments:True` เพื่อจัดการหน่วยความจำบนการ์ดจอ T4 ให้คุ้มค่าที่สุด
* **Granular Launch:** รัน ComfyUI ด้วย `highvram` และ `fp16` เพื่อความเสถียรสูงสุดในการเจนภาพ

---

## 🧠 Supported Engines
เลือกติดตั้ง Model ที่คุณต้องการผ่าน **Interactive Dropdown Menu**:

1.  **IDM-VTON:** เน้นความแม่นยำของรายละเอียดผ้าสูงที่สุด (มาพร้อม SAM และ ControlNet Aux)
2.  **CatVTON:** Lightweight & Fast ทำงานได้ไวบนทรัพยากรจำกัด
3.  **OOTDiffusion:** ระบบ Warping ที่เป็นธรรมชาติที่สุดสำหรับภาพคนจริง
4.  **FitDiT:** สถาปัตยกรรม Diffusion Transformer สำหรับการเก็บรายละเอียดรอยยับที่ซับซ้อน

---

## 🛠️ Installation Guide (Google Colab)

1.  **Preparation:** เปิด Notebook และตั้งค่า Runtime เป็น **T4 GPU** (เสมอ)
2.  **Model Selection:** เลือก `TARGET_NODE` ในเมนู Dropdown (เช่น IDM-VTON)
3.  **Run & Relax:** รัน Cell ทั้งหมด ระบบจะทำขั้นตอนดังนี้:
    * `[1/5]` เตรียม Core Environment และ ComfyUI Manager
    * `[2/5]` ฉีด Vaccine ป้องกัน Dependency พัง (Stability Fixes)
    * `[3/5]` โคลน Custom Nodes ตามโมเดลที่เลือก
    * `[4/5]` **The Hammer Fix:** บังคับลง Version ของ Transformers และ Diffusers ให้ตรงกับงานวิจัย
    * `[5/5]` เปิด Cloudflare Tunnel รับลิงก์ `*.trycloudflare.com`

---

## 🚀 System Optimizations (Behind the Scenes)
*(นั่งหน้าคอม)* สำหรับผู้ที่สนใจโครงสร้างวิศวกรรม:
* **Network:** ใช้ `aria2` มัลติเธรดดาวน์โหลดน้ำหนักโมเดลขนาดใหญ่ในหลักวินาที
* **Memory:** ป้องกัน Error "OutOfMemory" ด้วยการตั้งค่า `PYTORCH_CUDA_ALLOC_CONF`
* **Secure Access:** ใช้ Cloudflare Tunnel แทนการใช้ LocalTunnel เพื่อลดโอกาสลิงก์ตายระหว่างทำงาน

---

## 🤝 Credits & Acknowledgments
โปรเจกต์นี้เกิดขึ้นได้ด้วยการต่อยอดจากผลงานของเหล่ายักษ์ใหญ่ในวงการ:
* **Infrastructure Foundation:** [nazdridoy/ComfyUI-On-Colab](https://github.com/nazdridoy/ComfyUI-On-Colab)
* **Core UI:** [comfyanonymous](https://github.com/comfyanonymous/ComfyUI)
* **Research Teams:**
    * **IDM-VTON:** [yisol/IDM-VTON](https://github.com/yisol/IDM-VTON)
    * **CatVTON:** [chflame163/ComfyUI_CatVTON_Wrapper](https://github.com/chflame163/ComfyUI_CatVTON_Wrapper)
    * **OOTDiffusion:** [AuroBit/ComfyUI-OOTDiffusion](https://github.com/AuroBit/ComfyUI-OOTDiffusion)
    * **FitDiT:** [BoyuanJiang/FitDiT-ComfyUI](https://github.com/BoyuanJiang/FitDiT-ComfyUI)

---
*Developed & Patched by **nano** - Aiming for Production Excellence.*