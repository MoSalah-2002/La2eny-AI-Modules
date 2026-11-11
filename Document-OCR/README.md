# Document OCR — Contract Information Extraction

This module explores OCR-style extraction of structured information from contract images using a vision-language model hosted through the Hugging Face Inference API.

## Workflow
1. Load a contract/document image.
2. Encode the image and send it with Arabic extraction instructions.
3. Ask the model to return JSON, preserving empty fields and avoiding guesses.
4. Parse and save the structured result as UTF-8 JSON.

## Setup
```bash
pip install -r requirements.txt
```

Set `HUGGINGFACEHUB_API_TOKEN` in your environment before running the notebook. Never commit access tokens or private contract images.

## Notebook
- `notebooks/Contract_Document_OCR.ipynb`

## Notes
- The notebook uses the model endpoint shown in the original experiment; availability and access depend on the provider.
- This is an experimental extraction workflow, not a legal review system. Verify extracted fields manually.
- Test only with documents you are authorized to process, and remove personal information from public examples.
