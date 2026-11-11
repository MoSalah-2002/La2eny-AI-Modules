# 🔎 La2eny — AI Modules

<p align="center">
  <img src="https://img.shields.io/badge/Graduation%20Project-La2eny-0f766e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Domain-AI%20%26%20Computer%20Vision-2563eb?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Notebooks-Google%20Colab-f59e0b?style=for-the-badge" />
</p>

**La2eny (لاقيني)** is a community-oriented lost-and-found platform concept. This repository collects AI experiments and modules associated with the project, including face matching, visual similarity retrieval, document OCR, license-plate detection, and image captioning.

## ✨ AI Modules

| Module | Goal | Core approach |
|---|---|---|
| **Face Matching** | Compare a query face with reference images | Face encodings and face comparison |
| **Image Similarity** | Retrieve visually similar images | VGG16 deep features and cosine distance |
| **Document OCR** | Extract structured fields from contract images | Hugging Face vision-language inference and JSON parsing |
| **License Plate Detection** | Locate license plates in vehicle images | YOLOv8 object detection |
| **Image Captioning** | Generate descriptions of image content | LLaVA 1.5 vision-language model |

### 1. Face Matching
📁 [Face-Matching](Face-Matching/)

Loads a gallery of reference images, extracts face encodings, compares a query image against the gallery, and returns candidate matches.

**Notebook:** [Face_Matching_with_face_recognition.ipynb](Face-Matching/notebooks/Face_Matching_with_face_recognition.ipynb)

### 2. Image Similarity Search
📁 [Image-Similarity](Image-Similarity/)

Uses a pretrained VGG16 model to extract image representations from the `fc2` layer, then ranks candidate images using cosine distance.

**Notebook:** [VGG16_Image_Similarity_Search.ipynb](Image-Similarity/notebooks/VGG16_Image_Similarity_Search.ipynb)

### 3. Document OCR
📁 [Document-OCR](Document-OCR/)

Extracts contract fields from a document image, requests structured Arabic JSON output, and saves the parsed result as a JSON file.

**Notebook:** [Contract_Document_OCR.ipynb](Document-OCR/notebooks/Contract_Document_OCR.ipynb)

### 4. License Plate Detection
📁 [License-Plate-Detection](License-Plate-Detection/)

Downloads the original Roboflow dataset version and trains/validates a YOLOv8-large detector for license-plate localization.

**Notebook:** [YOLOv8_License_Plate_Detection.ipynb](License-Plate-Detection/notebooks/YOLOv8_License_Plate_Detection.ipynb)

### 5. Image Captioning
📁 [Image-Captioning](Image-Captioning/)

Uses LLaVA 1.5 to generate natural-language descriptions focused on the main subject in an image.

**Notebook:** [LLaVA_Image_Captioning.ipynb](Image-Captioning/notebooks/LLaVA_Image_Captioning.ipynb)

## 🗂️ Repository Structure

```text
La2eny-AI-Modules/
├── Face-Matching/
│   ├── notebooks/
│   └── requirements.txt
├── Image-Similarity/
│   ├── notebooks/
│   └── requirements.txt
├── Document-OCR/
│   ├── notebooks/
│   │   └── Contract_Document_OCR.ipynb
│   ├── README.md
│   └── requirements.txt
├── License-Plate-Detection/
│   ├── notebooks/
│   │   └── YOLOv8_License_Plate_Detection.ipynb
│   ├── README.md
│   └── requirements.txt
├── Image-Captioning/
│   ├── notebooks/
│   │   └── LLaVA_Image_Captioning.ipynb
│   ├── README.md
│   └── requirements.txt
├── .env.example
├── .gitignore
├── README.md
└── SECURITY_REVIEW.md
```

## ⚙️ Setup

The notebooks were originally prepared for Google Colab. Open the notebook for the module you want to run, install its requirements, and provide your own datasets/images and credentials where required.

Install dependencies for an individual module:

```bash
pip install -r Face-Matching/requirements.txt
pip install -r Image-Similarity/requirements.txt
pip install -r Document-OCR/requirements.txt
pip install -r License-Plate-Detection/requirements.txt
pip install -r Image-Captioning/requirements.txt
```

Some modules require external credentials:
- Document OCR: `HUGGINGFACEHUB_API_TOKEN`
- License Plate Detection: `ROBOFLOW_API_KEY`

Set these as environment variables in your runtime. Never paste real tokens into notebooks or commit them.

## 📂 Data & Models

Datasets, personal images, model weights, and generated feature files are intentionally excluded. Supply your own appropriately licensed test images and update paths in each notebook.

## 🛡️ Responsible Use & Privacy

Face matching, document extraction, and license-plate detection can involve sensitive personal information. These notebooks are experimental demonstrations, **not verified identity, legal, or law-enforcement systems**.

- Use images and documents only when you have the right to process them.
- Never treat a similarity score or OCR output as definitive proof.
- Require human review before acting on a possible match or extracted field.
- Keep missing-person reports, identity documents, and plate images private.
- Evaluate false matches, missed detections, and extraction errors on representative validation data.

## 🔐 Security

- Saved notebook outputs were cleared from the packaged notebooks.
- Hard-coded credentials found in the source archive were not copied into the cleaned notebooks.
- Required credentials are read from environment variables.
- Revoke or rotate any API key/token that appeared in the original archive; removing it from this repository does not invalidate it.
- Never commit real credentials, private datasets, or identity images.

See [SECURITY_REVIEW.md](SECURITY_REVIEW.md) for packaging checks and limitations.

## 🧪 Scope & Limitations

This repository is a cleaned portfolio snapshot of exploratory notebooks, not a production-ready application. The original datasets and trained weights are not included, and end-to-end execution has not been validated in a fresh environment. The OCR and captioning notebooks isolate the relevant experiments from a larger mixed notebook; unrelated application dependencies were left out.

## 🚀 Future Improvements

- Build reproducible data-preparation pipelines with privacy controls.
- Add unit tests and evaluation datasets for each module.
- Calibrate face-matching thresholds and report false-acceptance/false-rejection rates.
- Evaluate OCR field-level accuracy and plate-detection precision/recall.
- Refactor notebook code into tested Python modules and an API.
- Add demos using synthetic or explicitly licensed images.

---

<p align="center"><b>La2eny — Bringing lost things and people closer to being found.</b><br/><sub>Graduation Project · AI Development Team</sub></p>
