## Essential Concepts in Natural Language Processing and Generative AI

### Project Groundwork

This repository builds upon key foundations of Natural Language Processing (NLP): text embeddings, the transformer architecture at the core of large language models (LLMs), and Retrieval-Augmented Generation (RAG) for knowledge-grounded responses enhanced by prompt engineering.

- Embeddings: Text is represented as numerical vectors that encode meaning, similarity, and context for downstream NLP tasks. Classic methods like Word2Vec (CBOW/Skip-gram) and GloVe learn word relationships based on co-occurrence patterns (“a word is characterized by the company it keeps”). Contextual models like BERT extend this by making word vectors sentence-dependent, capturing nuanced meanings. Cosine similarity measures how closely word vectors relate in context.

- Transformers: A deep neural architecture using self-attention and positional encoding to model long-range dependencies and contextual relevance within sequences — the foundation of all modern LLMs.

- Large Language Models (LLMs): Transformer-based networks trained on web-scale text for language understanding and generation. They learn general patterns through pre-training, refine behavior through fine-tuning and RLHF, and are guided toward desired outputs via prompt engineering.

- Retrieval-Augmented Generation (RAG): Extends LLMs by grounding responses in external knowledge sources. It retrieves relevant data, augments the input prompt with that context, and generates responses that are more accurate and verifiable.

[![Alt text 1](NLP_fundamentals.png)](NLP_fundamentals.png)

## Problem Statement

Advancements in large language models (LLMs) are transforming the healthcare landscape by enabling intelligent solutions that efficiently process and interpret vast medical knowledge. This project explores the role of AI in healthcare through the development of a RAG based system designed to provide quick and reliable access to trusted medical information. By integrating established medical manuals into a centralized, AI-driven knowledge platform, the project aims to demonstrate how such technology can reduce information overload, enhance diagnostic efficiency, and support consistent, evidence-based clinical decision-making. The project seeks to highlight AI’s potential to improve patient care standards and overall healthcare outcomes through a practical, functional prototype.

### Data Description

- The dataset is derived from The Merck Manuals, medical references published by Merck & Co.
- It encompasses a comprehensive range of topics, including medical disorders, diagnostic procedures, laboratory tests, and pharmaceutical information.
- First published in 1899. The Merck Manuals have evolved into one of the most respected and widely used medical reference resources globally.
- The dataset is a PDF file containing over 4,000 pages, systematically organized into 23 sections to facilitate structured knowledge retrieval and analysis.

**Note**: The dataset used is not shared due to licensing restrictions. This notebook is compatible with any PDF files. The MERCK MANUAL OF DIAGNOSIS AND THERAPY can be found on third-party document sharing sites.

## Environment Setup

- It is recommended to use Google Colab for this Notebook. Google Colab offers ready-to-use environment that avoids the time-consuming and error-prone setup involved in local installations.

- To boost performance, make sure to set the runtime to use the T4 GPU.
    To ensure you're using the T4 GPU runtime in Google Colab, follow these steps:

    * From the menu bar at the top of the page, select `Runtime`.
    * In the dropdown menu that appears, select `Change runtime type`.
    * In the "Runtime type" dropdown within the dialog box, select `T4 GPU`.
    * Click the `Save` button.
    * ![](./colab_runtime_settings.png)

## About the Models Used in this Notebook

**llama-cpp-python** is a Python wrapper for llama.cpp, a universal LLM inference library that runs models efficiently using the GGUF file format.

**GGUF (GGML Universal File)** is a binary format storing model weights and metadata in a single file. It uses quantization to reduce precision, decreasing memory usage and increasing inference speed.

**Model Compatibility**: Supports any GGUF-converted model including Llama, Mistral, CodeLlama, Gemma, and Qwen.

**Key Components**:
- `Llama()` class: Main interface for loading and running models
- `hf_hub_download()`: A function from the Hugging Face Hub library to download specific files from Hugging Face repositories with automatic caching

**Models Used in This Notebook**

All models used are freely available from Hugging Face, requiring no API keys or credits.

| Model | Repository | File | Model card |
|-------|------------|------|---------|
| Mistral-7B-Instruct-v0.2 | `TheBloke/Mistral-7B-Instruct-v0.2-GGUF` | `mistral-7b-instruct-v0.2.Q6_K.gguf` | https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.2-GGUF |
| GTE-Large | `thenlper/gte-large` | SentenceTransformer | https://huggingface.co/thenlper/gte-large |
