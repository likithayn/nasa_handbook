# nasa_handbook
Advanced RAG Chatbot for the NASA Systems Engineering Handbook (SP-2016-6105 Rev2)  A robust Question-Answering system designed specifically for complex technical manuals.  Built to overcome the limitations of standard RAG when dealing with 270-page documents containing nested sections, multi-page tables, heavy cross-references, and dense acronyms.

# NASA Systems Engineering Handbook QA Chatbot

An intelligent chatbot that can answer questions from the official **270-page NASA Systems Engineering Handbook (SP-2016-6105 Rev2)**.

This project solves a real-world challenge: **Standard RAG systems fail on complex technical manuals** because of nested sections, multi-page tables, heavy cross-references, and dense acronyms. This chatbot is built to handle these difficulties effectively.

## What is this Project?

This is a Retrieval-Augmented Generation (RAG) based Question-Answering system specifically designed for technical handbooks.  
It allows users to ask natural language questions like:
- "What are the entry criteria for PDR?"
- "What should a verification plan include?"
- "How does risk management feed into technical reviews?"

And get accurate answers with proper sources.

## Architecture Overview

```mermaid
User Question
      ↓
Query Engine (LlamaIndex)
      ↓
Retrieval → Vector Store (Chroma)
      ↓
LlamaParse Documents → Local Embeddings (BAAI/bge-small-en-v1.5)
      ↓
Gemini 2.5 Flash + Custom Technical Prompt
      ↓
Answer + Sources
