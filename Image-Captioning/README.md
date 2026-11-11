# Image Captioning

This module focuses on generating natural-language descriptions of image content using the LLaVA 1.5 vision-language model.

## Workflow
1. Load an image with Pillow.
2. Load `llava-hf/llava-1.5-7b-hf` through the Transformers image-to-text pipeline.
3. Use 4-bit quantization to reduce memory requirements where supported.
4. Generate a concise description focused on the main subject.

## Setup
```bash
pip install -r requirements.txt
```

A CUDA-enabled PyTorch installation is recommended. The 7B model still requires substantial GPU memory even with 4-bit quantization.

## Notebook
- `notebooks/LLaVA_Image_Captioning.ipynb`

## Notes
- This notebook isolates the image-captioning portion of the original `imageToText.ipynb` experiment.
- The original notebook also contained clothing detection, ID/plate recognition, and private module dependencies; those unrelated components are intentionally not included here.
- Do not upload private images or credentials.
