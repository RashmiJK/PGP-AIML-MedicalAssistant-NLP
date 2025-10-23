## Essential Concepts in Natural Language Processing and Generative AI

Placeholder for concepts learnt during the course.

[![Alt text 1](NLP_fundamentals.jpg)](NLP_fundamentals.jpg)

## Problem Statement

Advancements in large language models (LLMs) are transforming the healthcare landscape by enabling intelligent solutions that efficiently process and interpret vast medical knowledge. This project explores the role of AI in healthcare through the development of a RAG based system designed to provide quick and reliable access to trusted medical information. By integrating established medical manuals into a centralized, AI-driven knowledge platform, the project aims to demonstrate how such technology can reduce information overload, enhance diagnostic efficiency, and support consistent, evidence-based clinical decision-making. The project seeks to highlight AI’s potential to improve patient care standards and overall healthcare outcomes through a practical, functional prototype.

### Data Description

- The dataset is derived from The Merck Manuals, medical references published by Merck & Co.
- It encompasses a comprehensive range of topics, including medical disorders, diagnostic procedures, laboratory tests, and pharmaceutical information.
- First published in 1899. The Merck Manuals have evolved into one of the most respected and widely used medical reference resources globally.
- The dataset is provided as a PDF file containing over 4,000 pages, systematically organized into 23 sections to facilitate structured knowledge retrieval and analysis.

### Environment Setup

- It is recommended to use Google Colab for this project. Google Colab offers ready-to-use environment that avoids the time-consuming and error-prone setup involved in local installations.
- It comes pre-configured with essential libraries, eliminating dependency conflicts and ensuring compatibility.
- To boost performance, make sure to set the runtime to use the T4 GPU.

1. Python virtual environment:

```bash
# Create a virtual environment
python -m venv .venv

# Activate the virtual environment
# On Windows
.venv\Scripts\activate
# On macOS/Linux
source .venv/bin/activate
```

2. Install Required Packages

After activating the virtual environment, install the necessary packages listed in `requirements.txt`:
```bash
pip install -r requirements.txt
```
```bash
pip install -r requirements.txt
```

3. Deactivate the Virtual Environment

To deactivate the virtual environment, simply run:

```bash
deactivate