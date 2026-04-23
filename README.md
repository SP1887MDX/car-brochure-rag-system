# Car Brochure RAG System

## Overview
This project implements a Retrieval-Augmented Generation (RAG) system that allows users to upload automotive brochure PDFs and ask questions about them.

The system retrieves relevant sections of the brochure and generates answers grounded strictly in the document.

---

## Features
- PDF upload and processing
- Text chunking and filtering
- Embeddings using HuggingFace
- FAISS vector search
- LangChain-based RAG pipeline
- Structured outputs
- Retrieval debugging (scores + chunks)
- Guardrails (prevents hallucinations)

---

## Example Questions
- What engine does this car have?
- What features are included?
- What type of driver is this car designed for?

---

## Tech Stack
- Python
- Google Colab
- LangChain
- FAISS
- HuggingFace Embeddings
- Groq LLM (Llama 3.1)

---

## How to Run
1. Open the notebook in Google Colab
2. Install dependencies
3. Enter API key
4. Upload brochure PDF
5. Run all cells

---

## Notes
The system only answers using retrieved brochure content. If information is missing, it will abstain.