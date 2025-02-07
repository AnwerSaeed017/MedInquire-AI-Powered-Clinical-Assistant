# MedInquire: AI-Powered Clinical Assistant

MedInquire is an AI-driven clinical assistant built in Google Colab that leverages state-of-the-art natural language processing to help answer clinical queries based on uploaded medical documents (such as text files and PDFs). The project uses retrieval-augmented generation to locate relevant passages from a collection of patient records and clinical texts, then uses the BioMistral-7B model (in a GGUF quantized format) to generate clear, concise answers.

## Features

- **Document Ingestion:** Loads medical text files (and PDFs) from a designated Google Drive folder.
- **Text Processing:** Splits documents into manageable chunks using a recursive character text splitter.
- **Vector Store:** Indexes document chunks using transformer-based embeddings (BAAI/bge-base-en-v1.5) and stores them in a Chroma vector store.
- **Retrieval:** Retrieves relevant document segments based on similarity search for a given clinical query.
- **Response Generation:** Uses the BioMistral-7B model (via llama_cpp) integrated with a custom prompt template to generate context-aware answers.
- **Flexible Querying:** Designed for medical professionals or researchers to query the system with clinical questions and receive evidence-based responses.

## Requirements

The project has been developed and tested in Google Colab. The following Python packages are required:
- `langchain`
- `sentence-transformers`
- `chromadb`
- `llama-cpp-python`
- `langchain_community`
- `pypdf`

You can install all dependencies using pip:

```bash
!pip install langchain sentence-transformers chromadb llama-cpp-python langchain_community pypdf
