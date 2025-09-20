# Meta-s-Segment-Anything-Model-SAM-with-stable-XL-diffusers-for-generative-image-editing-
Meta’s Segment Anything Model (SAM) with stable XL diffusers for generative image editing 
# SAM + Stable Diffusion XL Inpainting

This project combines **Meta’s Segment Anything Model (SAM)** for segmentation with **Stable Diffusion XL Inpainting** for generative image editing.  
The workflow allows you to select a region of an image (via point prompts) and replace it with new content guided by a text prompt.

---

## 🚀 Features
- Use **SAM** to create segmentation masks from user-provided points.
- Convert binary masks to RGBA for visualization.
- Apply **Stable Diffusion XL Inpainting** (`diffusers/stable-diffusion-xl-1.0-inpainting-0.1`) to fill in the masked regions.
- Control the generation with **text prompts**, **negative prompts**, and **guidance scale**.
- Deterministic results with fixed random seeds.

---

## 🛠️ Installation

### Prerequisites
- Python 3.9+
- CUDA-capable GPU with at least 8GB VRAM recommended

### Install dependencies
```bash
pip install torch torchvision --extra-index-url https://download.pytorch.org/whl/cu121
pip install transformers diffusers accelerate safetensors pillow
