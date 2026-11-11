# 🔎 La2eny — AI Modules

<p align="center">
  <img src="https://img.shields.io/badge/Graduation%20Project-La2eny-0f766e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Domain-Computer%20Vision-2563eb?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Notebooks-Google%20Colab-f59e0b?style=for-the-badge" />
</p>

**La2eny (لاقيني)** is a community-oriented lost-and-found platform concept. This repository presents two computer-vision modules developed as part of the graduation project: face matching and visual image-similarity retrieval.

## ✨ AI Modules

| Module | Goal | Core approach |
|---|---|---|
| **Face Matching** | Compare a query face with a gallery of reference images | Face detection, face encodings, and face comparison |
| **Image Similarity** | Retrieve visually similar images from a gallery | VGG16 deep features and cosine distance |

### 1. Face Matching
📁 [Face-Matching](Face-Matching/)

The notebook loads a gallery of reference images, extracts face encodings, compares a query image against the gallery, and returns a candidate match.

**Notebook:** [Face_Matching_with_face_recognition.ipynb](Face-Matching/notebooks/Face_Matching_with_face_recognition.ipynb)

**Dependencies:** `face-recognition`, `dlib`, OpenCV, NumPy, Matplotlib.

### 2. Image Similarity Search
📁 [Image-Similarity](Image-Similarity/)

The notebook uses a pretrained VGG16 model to extract image representations from the `fc2` layer, then ranks candidate images using cosine distance.

**Notebook:** [VGG16_Image_Similarity_Search.ipynb](Image-Similarity/notebooks/VGG16_Image_Similarity_Search.ipynb)

**Dependencies:** TensorFlow/Keras, SciPy, scikit-learn, NumPy, Matplotlib, Pillow.

## 🗂️ Repository Structure

```text
La2eny-AI-Modules/
├── Face-Matching/
│   ├── notebooks/
│   │   └── Face_Matching_with_face_recognition.ipynb
│   └── requirements.txt
├── Image-Similarity/
│   ├── notebooks/
│   │   └── VGG16_Image_Similarity_Search.ipynb
│   └── requirements.txt
├── .env.example
├── .gitignore
├── README.md
└── SECURITY_REVIEW.md
```

## ⚙️ Setup

The notebooks were originally prepared for Google Colab. Colab is recommended, especially for the `dlib` dependency used by face recognition.

### Google Colab
1. Open the notebook in the relevant module folder.
2. Upload your own test images and gallery to the session.
3. Update the image paths in the notebook.
4. Run the cells in order.

### Local environment
Create a virtual environment, then install the dependencies for the module you want to run:

```bash
python -m venv .venv
# Activate the environment, then:
pip install -r Face-Matching/requirements.txt
# or:
pip install -r Image-Similarity/requirements.txt
```

> Package compatibility depends on your Python version and operating system. The original notebooks have not been fully reproduced in a clean environment.

## 📂 Data & Models

Datasets, personal images, model weights, and generated feature files are intentionally excluded. Supply your own appropriately licensed test images and update the paths in each notebook.

## 🛡️ Responsible Use & Privacy

Face matching is a sensitive capability. These notebooks are experimental demonstrations, **not verified identity systems**.

- Use images only with an appropriate legal basis and consent.
- Never treat a similarity score as proof of identity.
- Require human review before acting on a possible match.
- Keep missing-person reports and identity images private.
- Evaluate false matches and missed matches on a representative validation set.

## 🔐 Security

- Saved notebook outputs were cleared before packaging.
- Credential-like patterns were scanned and sanitized in the packaged notebooks.
- No API credentials are required by the included modules.
- Never commit real credentials, private datasets, or identity images.
- Revoke any credential that may have been exposed in an earlier version; removing it from a new commit does not invalidate it.

See [SECURITY_REVIEW.md](SECURITY_REVIEW.md) for the packaging checks and limitations.

## 🧪 Scope & Limitations

This repository is a cleaned portfolio snapshot of exploratory notebooks, not a production-ready application. The original datasets and trained weights are not included, and end-to-end execution has not been validated in a fresh environment.

## 🚀 Future Improvements

- Build a reproducible data-preparation pipeline with privacy controls.
- Calibrate similarity thresholds on representative validation data.
- Evaluate face matching with precision, recall, false-acceptance, and false-rejection rates.
- Refactor notebook code into tested Python modules and an API.
- Add a demo using synthetic or explicitly licensed images.

---

<p align="center"><b>La2eny — Bringing lost things and people closer to being found.</b><br/><sub>Graduation Project · AI Development Team</sub></p>
