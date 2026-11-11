# License Plate Detection

This module contains the YOLOv8 license-plate object-detection training experiment from the original project archive.

## Workflow
1. Authenticate to Roboflow using an environment variable.
2. Download version 3 of the `plate-detect-oydq2` dataset in YOLOv8 format.
3. Train a YOLOv8-large detector.
4. Validate the trained weights against the downloaded dataset configuration.

## Setup
```bash
pip install -r requirements.txt
```

Set `ROBOFLOW_API_KEY` in your environment. The notebook does not contain the original hard-coded API key.

## Notebook
- `notebooks/YOLOv8_License_Plate_Detection.ipynb`

## Notes
- The notebook preserves the original workspace/project/version and training settings, but uses environment variables for credentials.
- Dataset download and training require Roboflow access and a compatible GPU/runtime.
- Detection identifies plate regions; it does not perform character recognition (OCR).
