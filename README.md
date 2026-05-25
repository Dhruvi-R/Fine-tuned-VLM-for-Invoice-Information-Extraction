# Fine-tuned-VLM-for-Invoice-Information-Extraction

## Overview
This project focuses on extracting structured information from invoice images using the Vision-Language Model (VLM) **Qwen2.5-VL**. The notebook demonstrates how to load an invoice dataset, preprocess invoice images, perform inference using a pretrained model, and generate structured JSON outputs from invoice documents.

The project also includes steps for:
- Loading and exploring the invoice dataset
- Running inference on invoice images
- Extracting invoice fields in JSON format
- Fine-tuning the Qwen2.5-VL model using LoRA with the Unsloth framework
- Evaluating model outputs for schema-specific generation tasks

---

## Features
- Invoice image understanding using Vision-Language Models (VLMs)
- Structured data extraction from invoices
- JSON-based output generation
- Support for fine-tuning with LoRA
- GPU acceleration support
- Hugging Face Transformers integration
- Dataset handling with Hugging Face Datasets

---

## Technologies Used
- Python
- PyTorch
- Hugging Face Transformers
- Qwen2.5-VL
- Unsloth
- Accelerate
- Pillow
- Hugging Face Datasets

---

## Dataset
The notebook uses the following dataset:
- `katanaml-org/invoices-donut-data-v1`

The dataset contains invoice images along with structured ground truth annotations for training and evaluation.

---

## Project Workflow

### 1. Load Dataset
The dataset is loaded using the Hugging Face `datasets` library.

### 2. Explore Invoice Images
Invoice images are visualized and corresponding ground truth annotations are inspected.

### 3. Load Qwen2.5-VL Model
The pretrained Qwen2.5-VL model and processor are initialized for inference.

### 4. Perform Invoice Extraction
The model generates structured outputs from invoice images.

### 5. Fine-Tuning with LoRA
The notebook demonstrates parameter-efficient fine-tuning using:
- LoRA (Low-Rank Adaptation)
- Unsloth Framework

### 6. Evaluate Outputs
Generated outputs are compared against expected invoice schema structures.

---

## Installation
Install the required dependencies:

```bash
pip install transformers accelerate datasets pillow
pip install qwen-vl-utils
pip install unsloth
```

For GPU support:

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
```

---

## Model Used
- **Qwen2.5-VL**

This model is capable of understanding both visual and textual information, making it suitable for document understanding and invoice extraction tasks.

---

## Example Output
Example structured JSON output:

```json
{
  "invoice_number": "INV-1024",
  "invoice_date": "2025-01-10",
  "vendor_name": "ABC Pvt Ltd",
  "total_amount": "₹12,500"
}
```


---

## Use Cases
- Automated invoice processing
- OCR enhancement with VLMs
- Financial document analysis
- Intelligent document understanding
- Enterprise workflow automation

---

## Future Improvements
- Improve extraction accuracy with larger datasets
- Add support for multilingual invoices
- Deploy as a web application using Streamlit or Gradio
- Add evaluation metrics for extraction performance
- Integrate database storage for extracted invoice data

---

## Author
Dhruvi Rupera

---

## License
This project is intended for educational and research purposes.
