# Car Brochure RAG System

## Overview
This project implements a Retrieval-Augmented Generation (RAG) system that allows users to upload automotive brochure PDFs and ask structured questions about their content.

The system retrieves relevant sections of the brochure using semantic search and generates answers grounded strictly in the retrieved document context.

---

## Problem Statement
Automotive brochures contain detailed information about vehicle specifications, features, and design, but extracting specific information manually can be time-consuming and inefficient.

This project addresses this by enabling targeted question answering directly over brochure content.

---

## Solution Approach
The system follows a standard RAG pipeline:

1. Load brochure PDF
2. Split text into manageable chunks
3. Convert chunks into vector embeddings
4. Store embeddings in a FAISS vector database
5. Retrieve relevant chunks for a given query
6. Generate a structured answer using an LLM

A lightweight reliability mechanism is included to prevent unsupported answers.

---

## Features
- PDF upload and processing
- Text chunking and filtering
- HuggingFace embeddings (`all-MiniLM-L6-v2`)
- FAISS vector store
- LangChain-based RAG pipeline
- Structured response formatting
- Retrieval debugging (scores + chunks)
- Guardrails to reduce hallucination

---

## Example Queries
- What engine does this car have?
- What interior features are included?
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
2. Run the setup section
3. Provide API key when prompted
4. Upload a brochure PDF
5. Execute all cells
6. Run the example queries or enter a custom question

---

## System Behaviour
The system is designed to:
- Answer only using retrieved brochure content
- Avoid generating unsupported information
- Return a structured response format

If insufficient evidence is found, the system will abstain from answering.

---

## Limitations
- Performance depends on the quality of the uploaded brochure
- Retrieval may miss relevant sections if phrasing differs significantly
- Interpretive answers are limited to what can be inferred from the brochure text

---

## Conclusion
This project demonstrates a clean and focused implementation of a RAG system using lecture-aligned methods. It prioritises reliability, modularity, and grounded responses, making it suitable for both demonstration and evaluation in a hackathon setting.