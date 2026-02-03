# Imagine – Context-Aware Image Generation

Imagine is a context-aware image generation system built using Stable Diffusion and DreamBooth. It focuses on personalized and realistic image synthesis by learning a specific subject and generating it across diverse environments while preserving identity and semantic consistency.

The system is developed in Python using Hugging Face Diffusers and PyTorch. It fine-tunes the pre-trained `CompVis/stable-diffusion-v1-4` model on a custom instance dataset (`diffusers/dog-example`) along with class images generated for prior preservation. This enables high-quality subject-aware and context-driven image generation.

---

## Key Features

- Personalized subject learning using DreamBooth  
- Context-based environment adaptation  
- Identity preservation across scenes  
- High-quality realistic synthesis  
- Memory-efficient training on limited GPUs  
- Hugging Face integration  

---

## Technologies

- Python  
- PyTorch  
- Stable Diffusion  
- Hugging Face Diffusers  
- DreamBooth  
- Transformers  
- Accelerate  
- xFormers  
- BitsAndBytes  
- CUDA  

---

## Hardware Requirements

- NVIDIA GPU with CUDA support (minimum 8 GB VRAM, 12 GB+ recommended)  
- CUDA Toolkit 11.7 or newer  
- Compatible NVIDIA Driver  
- Minimum 16 GB system RAM (32 GB recommended for training)  
- At least 20 GB free disk space for models and datasets  
- Tested on Linux and Google Colab (limited support on Windows WSL)

> Note: CPU-only execution is not recommended due to high computational requirements.

---

## Dataset and Model

- Instance Dataset: `diffusers/dog-example` (Hugging Face)
- Class Dataset: Auto-generated (prior preservation)
- Base Model: `CompVis/stable-diffusion-v1-4`
- Fine-Tuning Method: DreamBooth

---

## Sample Inputs and Outputs

### Input Images (Training Samples)

![image](https://github.com/user-attachments/assets/b4444fe7-9f49-438a-8064-ab4bfe62fec3)
![image](https://github.com/user-attachments/assets/05937b9e-c0c7-48d2-b854-09a71306a612)
![image](https://github.com/user-attachments/assets/66406891-90a1-4d18-bb6c-bbc84705422b)
![image](https://github.com/user-attachments/assets/e00121f8-c794-473e-bd75-77727dad62d4)
![image](https://github.com/user-attachments/assets/954e6b3c-22e7-4e09-a16f-097f3189b34c)

### Generated Outputs

| Prompt | Output |
|--------|--------|
| dog in in beach | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/6fb668f8-8846-4d8b-a443-c91c4a5119c9" /> |
| dog in in living room | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/67cdcbb1-6e18-4e4e-ab3f-8358354814d8" /> |
| my dog teddy in park | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/350d5ef4-27e0-4366-a443-c6dbc1d1ae45" /> |
| my dog teddy in beach | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/30d2c443-37d7-4525-adce-64f964aa4559" /> |
| my dog teddy playing in beach | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/ea8c087b-f92d-489b-8e31-a398bd00d679" /> |
| my dog teddy in lawn | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/82efcf7e-52f8-4c09-b4fa-05197371eb4b" /> |
| my dog teddy in snow | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/d5c04190-0486-46a2-843d-2d2ad7d9017e" /> |
| tiger in beach (Random prompt without specifying name of trained subject) | <img width="512" height="512" alt="download" src="https://github.com/user-attachments/assets/526e9046-a5c6-431b-a0b0-7bd195b0b663" /> |

---

## Setup and Installation

### Clone the Repository
```bash
git clone https://github.com/krharitej/Imagine.git
cd Imagine
```

### Running the Project
Training (Optional – For Custom Subjects)
```bash
accelerate launch Imagine.py
```
- Ensure dataset paths are correctly configured before training

Inference / Image Generation
```bash
python Imagine.py
```
Or run using Jupyter:
```bash
jupyter notebook Imagine.ipynb
```

---

## System Workflow
Input Images + Prompts → DreamBooth Fine-Tuning → Custom Model → Context-Aware Image Output

---

## Author

**K R Haritej**  

---

## 📜 License

This project is intended for educational and research purposes.  
Please refer to the respective licenses of Stable Diffusion and DreamBooth.
