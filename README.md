# Object Detection using Azure Computer Vision
### SIG788 — Engineering AI Solutions | Deakin University

## Overview
This project implements an object detection pipeline using the **Azure Computer Vision API (v3.2)**. Given an input image, the system detects objects, draws colour-coded bounding boxes, and exports structured results in CSV and JSON formats.

Built as part of the Master of Data Science program at Deakin University.

---

## What It Does
- Sends an image to Azure Computer Vision's `/detect` endpoint
- Parses the JSON response to extract detected objects, confidence scores, and bounding box coordinates
- Annotates the original image with colour-coded bounding boxes and labels
- Exports results as:
  - `detected_objects_output.jpg` — annotated image
  - `detection_results.csv` — tabular results (Excel-compatible)
  - `detection_results.json` — structured JSON output
- Generates a summary report of detection statistics

---

## Tech Stack
- **Python** — requests, Pillow, Pandas
- **Azure Computer Vision API** — v3.2 detect endpoint
- **Jupyter Notebook**

---

## Setup

### 1. Clone the repo
```bash
git clone https://github.com/isahid11/Object-Detection-Azure-Computer-Vision.git
cd Object-Detection-Azure-Computer-Vision
```

### 2. Install dependencies
```bash
pip install requests Pillow pandas python-dotenv
```

### 3. Configure credentials
Create a `.env` file in the root directory:
```
AZURE_ENDPOINT=https://your-resource.cognitiveservices.azure.com/
AZURE_API_KEY=your_api_key_here
```
> Get these from your Azure Portal under your Computer Vision resource.

### 4. Add your test image
Place a `test_image.jpg` in the same directory as the notebook.

### 5. Run the notebook
```bash
jupyter notebook Task5D_Object_Detection_Azure.ipynb
```

---

## Project Structure
```
├── Task5D_Object_Detection_Azure.ipynb   # Main notebook
├── .env.example                          # Template for credentials
├── .gitignore                            # Excludes .env and output files
└── README.md
```

---

## Key Findings
- Successfully detected multiple object classes with confidence scores and precise bounding box coordinates
- Evaluated model performance across varied image types and lighting conditions
- Identified limitations around small objects, occlusion, and low-contrast scenes
- Discussed trade-offs between API-based solutions vs. custom-trained models (YOLO, Faster R-CNN)

---

## Skills Demonstrated
- REST API integration and HTTP request handling
- Image processing and annotation with Pillow
- JSON parsing and structured data export
- Model output evaluation and confidence analysis
- Technical documentation and report writing
